# Date/Time Picker v4.17.47
Fork to use with Tailwind CSS / Turbolinks / Laravel LiveWire

# Use with Turbolinks and Laravel LiveWire:

Script:

    <script type="text/javascript">
        function Datepicker() {
            $('#datetimepicker').datetimepicker({
                format: 'YYYY-MM-DD H:mm'
            }).on("dp.change", function (e) {
                @this.set('pay_date', e.date);
            });
        };
        window.addEventListener('turbolinks:load', Datepicker);
    </script>
    
HTML:

    <div style="position: relative;">
        <label>
            <div wire:ignore>
                <input  type="text" class="form-input block w-full text-xs" placeholder="{{ __('Pay Date') }}"  id="datetimepicker">
            </div>
        </label>
    </div>