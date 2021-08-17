---
title: 執行裝置行為
description: 裝置的行為是由它所公開的服務所定義。
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce2857c11a02ef5eeebe7b2cd5e75ee76138929e5bd95a2e3bdfa7ffd2c71dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137261"
---
# <a name="implementing-device-behavior"></a>執行裝置行為

裝置的行為是由它所公開的服務所定義。 每個服務都有列出其動作和狀態變數的服務描述。 這些服務描述會結合在一起，以定義控制點可以與服務互動的方式。 每個服務都必須至少有一個動作。

若要執行服務，託管裝置必須提供元件物件模型 (COM) 物件，此物件會公開服務的介面。 在服務描述中，服務介面是以 UPnP 範本語言指定 (UTL) ;不過，COM 物件介面通常是以介面定義語言 (IDL) 指定。 您也可以指定類型程式庫或標頭檔中的 COM 介面。 平臺軟體發展工具組 (SDK) 包含 Utl2idl 工具，此工具會將 UTL 中的服務描述轉譯為 IDL 中的 COM 介面。

下列範例說明這項轉換程式。 服務描述是由裝置開發人員提供，並以 UTL 撰寫。

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

下一步是執行 Utl2idl 工具。 它會產生包含 COM 介面的 IDL 檔案。 如需 IDL 檔案和 **interface** 關鍵字的詳細資訊，請參閱 MIDL 參考中的 [ (idl)](/windows/desktop/Midl/interface-definition-idl-file) 檔案和 [**介面**](/windows/desktop/Midl/interface) 的介面定義。

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> 傳回值是 \[ \] 服務描述中引數清單中的第一個 out 參數，不過，它在轉譯之後會列為最後一個參數。
> 
> 所有其他參數會維持相同的順序。

 

若要提供服務的功能，請執行這個 COM 介面。

## <a name="obtaining-information-about-an-endpoint"></a>取得端點的相關資訊

在 UPnP 架構中，端點資訊包含要求和其來源的相關資訊。 裝置可以檢查這項資訊，以便決定要求的相關資訊。

端點資訊可選擇性地用於已執行的服務。 裝置主機具有端點資訊的存取權;不過，裝置主機預設不會將資訊傳送至已實行的服務。 您可以藉由在 Utl2idl 工具) 所產生的 IDL 檔案 (中修改 COM 介面，讓裝置主機與已執行的服務共用端點資訊。 您可以將 \[ in \] 參數加入至需要端點資訊的每個方法。 其他 \[ in \] 參數必須是引數清單中的第一個參數、 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面的指標，以及明確命名的 **punkRemoteEndpointInfo**。 對服務 XML 的修改並非必要或建議。 下列範例會顯示修改後的 **PowerOn** 方法新定義，以便接收端點資訊：

"HRESULT PowerOn (\[ in \] IUnknown \* punkRemoteEndpointInfo) ;"

端點資訊物件的指標，也就是 [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) 介面，由裝置主機透過這個新的參數傳遞。 **IUPnPRemoteEndpointInfo** 介面提供三種方法來存取端點資訊。 您必須呼叫適當的方法，才能取得服務執行所需的端點資訊。

除了手動修改 COM 介面，您也可以搭配使用 Utl2idl 工具與 **-ci** 參數。 此參數會使工具將端點資訊參數新增至 COM 介面中的每個方法。 使用 **-ci** 參數不有助於修改個別方法。 如果介面的所有方法都不需要端點資訊，您應該手動加入參數，以產生最有效率的執行。

## <a name="implementing-a-service-object"></a>執行服務物件

您必須使用 Utl2idl 工具來轉譯裝置的每個服務描述。

提供服務功能的物件稱為「 [*服務物件」（service object*](s-gly.md)）。 除了提供服務功能之外，服務物件還會使用 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面來處理錯誤。 如需詳細資訊，請參閱 [使用裝置主機 API 搭配 UPnP 技術](using-the-device-host-api-with-upnp-technology.md)。

為了確保與不支援 out 參數的 Visual Basic 的相容性 \[ \] ，服務描述中的 **方向** 輸出 **/direction** 參數會轉換成 IDL 中的 \[ in、out \] 參數。 伺服器必須釋放這些 \[ in、out \] 參數。

## <a name="implementing-a-device-control-object"></a>執行裝置控制物件

除了執行服務物件之外，您還必須執行 [*裝置控制物件*](d-gly.md)。 裝置控制物件是裝置服務物件管理和控制的中心點。 在註冊時，裝置控制物件會傳遞至裝置主機。 當事件訂用帳戶或控制項要求抵達其中一個裝置的服務時，裝置主機會呼叫此裝置控制物件以取得相關的服務物件。 屆時，裝置控制物件會建立服務物件的實例，或傳回服務物件之現有實例的介面。

您可以在多部電腦上或在同一部電腦上多次註冊裝置描述。 由於唯一的裝置名稱 (UDN) 必須與裝置的每個實例不同，因此裝置主機會在每次裝置註冊時，為每個裝置和內嵌的裝置產生唯一的 UDN。 使用裝置描述範本中指定的 UDN，來取得裝置主機所產生並與裝置建立關聯的實際 UDN。 若要取消註冊裝置，您必須使用 UPnP 架構在註冊裝置時所提供的識別碼。

裝置控制物件必須執行 [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) 介面。 裝置主機會叫用裝置控制物件的 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法，傳入裝置主機先前針對裝置所發佈的 UPnP 裝置描述，以及在註冊時指定的初始化字串 (查看 [向裝置主機註冊託管裝置](registering-a-hosted-device-with-the-device-host.md)) 。 在此裝置說明中，裝置控制物件會讀取指派給裝置樹狀結構中每個裝置的 UDNs。 您也可以使用 [**IUPnPRegistrar：： GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) 方法來取得此資訊。

當裝置主機需要服務物件的指標來執行特定服務時，它會在裝置控制物件上叫用 [**IUPnPDeviceControl：： GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) 方法。 裝置主機會傳遞 UDN，以及它要求服務物件之服務的服務識別碼，以及該方法預期會傳回服務物件指標的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標位址。 UDN 參數是必要的，因為裝置控制物件會管理整個裝置樹狀結構的服務，包括嵌套的裝置。 如果裝置主機要求嵌套裝置， **GetServiceObject** 會使用 UDN 來識別該裝置。

 

 