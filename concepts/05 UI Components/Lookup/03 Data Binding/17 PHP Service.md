DevExtreme provides the <a href="https://github.com/DevExpress/DevExtreme-PHP-Data/blob/master/README.md" target="_blank">DevExtreme-PHP-Data</a> extension that implements data processing on a PHP server according to the protocol the Lookup uses. To access the server from the client, configure the [CustomStore](/api-reference/30%20Data%20Layer/CustomStore '/Documentation/ApiReference/Data_Layer/CustomStore/') as described in the [Custom Sources](/concepts/70%20Data%20Binding/00%20Specify%20a%20Data%20Source/60%20Custom%20Data%20Sources '/Documentation/Guide/Data_Binding/Specify_a_Data_Source/Custom_Data_Sources/') article or use the <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/docs/client-side-with-jquery.md#api-reference" target="_blank">createStore</a> method. This method is a part of the <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/README.md" target="_blank">DevExtreme.AspNet.Data</a> extension. The following code shows how to use this method.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        const serviceUrl = "http://url/to/my/service.php";
        $("#lookupContainer").dxLookup({
            dataSource: DevExpress.data.AspNet.createStore({
                key: "ID",
                loadUrl: serviceUrl
            }),
            // ...
        })
    });

##### Angular

    <!--HTML-->
    <dx-lookup ...
        [dataSource]="store">
    </dx-lookup>

    <!--TypeScript-->
    import { DxLookupModule } from "devextreme-angular";
    import CustomStore from "devextreme/data/custom_store";
    import { createStore } from "devextreme-aspnet-data-nojquery";
    // ...
    export class AppComponent {
        store: CustomStore;
        constructor() {
            const serviceUrl = "http://url/to/my/service.php";
            this.store = createStore({
                key: "ID",
                loadUrl: serviceUrl
            })
        }
    }
    @NgModule({
        imports: [
            // ...
            DxLookupModule
        ],
        // ...
    })

##### Vue

    <template>
        <DxLookup ...
            :data-source="store"
        />
    </template>

    <script>
    import 'devextreme/dist/css/dx.common.css';
    import 'devextreme/dist/css/dx.light.css';

    import { DxLookup } from 'devextreme-vue/lookup';
    import { createStore } from "devextreme-aspnet-data-nojquery";

    const serviceUrl = "http://url/to/my/service.php";

    export default {
        components: {
            DxLookup
        },
        data() {
            return {
                store: createStore({
                    key: "ID",
                    loadUrl: serviceUrl
                })
            };
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.common.css';
    import 'devextreme/dist/css/dx.light.css';

    import { Lookup } from 'devextreme-react/lookup';
    import { createStore } from "devextreme-aspnet-data-nojquery";

    const serviceUrl = "http://url/to/my/service.php";

    class App extends React.Component {
        constructor(props) {
            super(props);

            this.store = createStore({
                key: "ID",
                loadUrl: serviceUrl
            });
        }

        render() {
            return (
                <Lookup ...
                    dataSource={this.store}
                />
            );
        }
    }

    export default App;

---
