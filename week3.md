<div class="panel-body">
    <div id="app" class="panel" style="border: 1px solid lightgray; min-height: 800px;"></div>
</div>

<script type="module">
    import 'https://editor.verovio.org/javascript/app/verovio-app.js';

    // Create the app - here with an empty option object
    const app = new Verovio.App(document.getElementById("app"), {});

    // Load a file (MEI or MusicXML)
    fetch("https://github.com/lordofanywhere/MCA-2023/blob/master/resources/When%20You%20Were%20Young.mei")
        .then(function(response) {
            return response.text();
        })
        .then(function(text) {
            app.loadData(text);
        });
</script>
 
