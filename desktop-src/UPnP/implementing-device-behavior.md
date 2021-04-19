---
title: 執行裝置行為
description: 裝置的行為是由它所公開的服務所定義。
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974779"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="da15d-103">執行裝置行為</span><span class="sxs-lookup"><span data-stu-id="da15d-103">Implementing Device Behavior</span></span>

<span data-ttu-id="da15d-104">裝置的行為是由它所公開的服務所定義。</span><span class="sxs-lookup"><span data-stu-id="da15d-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="da15d-105">每個服務都有列出其動作和狀態變數的服務描述。</span><span class="sxs-lookup"><span data-stu-id="da15d-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="da15d-106">這些服務描述會結合在一起，以定義控制點可以與服務互動的方式。</span><span class="sxs-lookup"><span data-stu-id="da15d-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="da15d-107">每個服務都必須至少有一個動作。</span><span class="sxs-lookup"><span data-stu-id="da15d-107">Each service must have at least one action.</span></span>

<span data-ttu-id="da15d-108">若要執行服務，託管裝置必須提供元件物件模型 (COM) 物件，此物件會公開服務的介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="da15d-109">在服務描述中，服務介面是以 UPnP 範本語言指定 (UTL) ;不過，COM 物件介面通常是以介面定義語言 (IDL) 指定。</span><span class="sxs-lookup"><span data-stu-id="da15d-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="da15d-110">您也可以指定類型程式庫或標頭檔中的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="da15d-111">平臺軟體發展工具組 (SDK) 包含 Utl2idl 工具，此工具會將 UTL 中的服務描述轉譯為 IDL 中的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="da15d-112">下列範例說明這項轉換程式。</span><span class="sxs-lookup"><span data-stu-id="da15d-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="da15d-113">服務描述是由裝置開發人員提供，並以 UTL 撰寫。</span><span class="sxs-lookup"><span data-stu-id="da15d-113">The service description is provided by the device developer and is written in UTL.</span></span>

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

<span data-ttu-id="da15d-114">下一步是執行 Utl2idl 工具。</span><span class="sxs-lookup"><span data-stu-id="da15d-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="da15d-115">它會產生包含 COM 介面的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="da15d-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="da15d-116">如需 IDL 檔案和 **interface** 關鍵字的詳細資訊，請參閱 MIDL 參考中的 [ (idl)](/windows/desktop/Midl/interface-definition-idl-file) 檔案和 [**介面**](/windows/desktop/Midl/interface) 的介面定義。</span><span class="sxs-lookup"><span data-stu-id="da15d-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

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
> <span data-ttu-id="da15d-117">傳回值是 \[ \] 服務描述中引數清單中的第一個 out 參數，不過，它在轉譯之後會列為最後一個參數。</span><span class="sxs-lookup"><span data-stu-id="da15d-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="da15d-118">所有其他參數會維持相同的順序。</span><span class="sxs-lookup"><span data-stu-id="da15d-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="da15d-119">若要提供服務的功能，請執行這個 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="da15d-120">取得端點的相關資訊</span><span class="sxs-lookup"><span data-stu-id="da15d-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="da15d-121">在 UPnP 架構中，端點資訊包含要求和其來源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="da15d-122">裝置可以檢查這項資訊，以便決定要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="da15d-123">端點資訊可選擇性地用於已執行的服務。</span><span class="sxs-lookup"><span data-stu-id="da15d-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="da15d-124">裝置主機具有端點資訊的存取權;不過，裝置主機預設不會將資訊傳送至已實行的服務。</span><span class="sxs-lookup"><span data-stu-id="da15d-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="da15d-125">您可以藉由在 Utl2idl 工具) 所產生的 IDL 檔案 (中修改 COM 介面，讓裝置主機與已執行的服務共用端點資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="da15d-126">您可以將 \[ in \] 參數加入至需要端點資訊的每個方法。</span><span class="sxs-lookup"><span data-stu-id="da15d-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="da15d-127">其他 \[ in \] 參數必須是引數清單中的第一個參數、 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面的指標，以及明確命名的 **punkRemoteEndpointInfo**。</span><span class="sxs-lookup"><span data-stu-id="da15d-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="da15d-128">對服務 XML 的修改並非必要或建議。</span><span class="sxs-lookup"><span data-stu-id="da15d-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="da15d-129">下列範例會顯示修改後的 **PowerOn** 方法新定義，以便接收端點資訊：</span><span class="sxs-lookup"><span data-stu-id="da15d-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="da15d-130">"HRESULT PowerOn (\[ in \] IUnknown \* punkRemoteEndpointInfo) ;"</span><span class="sxs-lookup"><span data-stu-id="da15d-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="da15d-131">端點資訊物件的指標，也就是 [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) 介面，由裝置主機透過這個新的參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="da15d-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="da15d-132">**IUPnPRemoteEndpointInfo** 介面提供三種方法來存取端點資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="da15d-133">您必須呼叫適當的方法，才能取得服務執行所需的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="da15d-134">除了手動修改 COM 介面，您也可以搭配使用 Utl2idl 工具與 **-ci** 參數。</span><span class="sxs-lookup"><span data-stu-id="da15d-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="da15d-135">此參數會使工具將端點資訊參數新增至 COM 介面中的每個方法。</span><span class="sxs-lookup"><span data-stu-id="da15d-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="da15d-136">使用 **-ci** 參數不有助於修改個別方法。</span><span class="sxs-lookup"><span data-stu-id="da15d-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="da15d-137">如果介面的所有方法都不需要端點資訊，您應該手動加入參數，以產生最有效率的執行。</span><span class="sxs-lookup"><span data-stu-id="da15d-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="da15d-138">執行服務物件</span><span class="sxs-lookup"><span data-stu-id="da15d-138">Implementing a Service Object</span></span>

<span data-ttu-id="da15d-139">您必須使用 Utl2idl 工具來轉譯裝置的每個服務描述。</span><span class="sxs-lookup"><span data-stu-id="da15d-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="da15d-140">提供服務功能的物件稱為「 [*服務物件」（service object*](s-gly.md)）。</span><span class="sxs-lookup"><span data-stu-id="da15d-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="da15d-141">除了提供服務功能之外，服務物件還會使用 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面來處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="da15d-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="da15d-142">如需詳細資訊，請參閱 [使用裝置主機 API 搭配 UPnP 技術](using-the-device-host-api-with-upnp-technology.md)。</span><span class="sxs-lookup"><span data-stu-id="da15d-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="da15d-143">為了確保與不支援 out 參數的 Visual Basic 的相容性 \[ \] ，服務描述中的 **方向** 輸出 **/DIRECTION** 參數會轉換成 IDL 中的 \[ in、out \] 參數。</span><span class="sxs-lookup"><span data-stu-id="da15d-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="da15d-144">伺服器必須釋放這些 \[ in、out \] 參數。</span><span class="sxs-lookup"><span data-stu-id="da15d-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="da15d-145">執行裝置控制物件</span><span class="sxs-lookup"><span data-stu-id="da15d-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="da15d-146">除了執行服務物件之外，您還必須執行 [*裝置控制物件*](d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="da15d-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="da15d-147">裝置控制物件是裝置服務物件管理和控制的中心點。</span><span class="sxs-lookup"><span data-stu-id="da15d-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="da15d-148">在註冊時，裝置控制物件會傳遞至裝置主機。</span><span class="sxs-lookup"><span data-stu-id="da15d-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="da15d-149">當事件訂用帳戶或控制項要求抵達其中一個裝置的服務時，裝置主機會呼叫此裝置控制物件以取得相關的服務物件。</span><span class="sxs-lookup"><span data-stu-id="da15d-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="da15d-150">屆時，裝置控制物件會建立服務物件的實例，或傳回服務物件之現有實例的介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="da15d-151">您可以在多部電腦上或在同一部電腦上多次註冊裝置描述。</span><span class="sxs-lookup"><span data-stu-id="da15d-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="da15d-152">由於唯一的裝置名稱 (UDN) 必須與裝置的每個實例不同，因此裝置主機會在每次裝置註冊時，為每個裝置和內嵌的裝置產生唯一的 UDN。</span><span class="sxs-lookup"><span data-stu-id="da15d-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="da15d-153">使用裝置描述範本中指定的 UDN，來取得裝置主機所產生並與裝置建立關聯的實際 UDN。</span><span class="sxs-lookup"><span data-stu-id="da15d-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="da15d-154">若要取消註冊裝置，您必須使用 UPnP 架構在註冊裝置時所提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="da15d-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="da15d-155">裝置控制物件必須執行 [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="da15d-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="da15d-156">裝置主機會叫用裝置控制物件的 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法，傳入裝置主機先前針對裝置所發佈的 UPnP 裝置描述，以及在註冊時指定的初始化字串 (查看 [向裝置主機註冊託管裝置](registering-a-hosted-device-with-the-device-host.md)) 。</span><span class="sxs-lookup"><span data-stu-id="da15d-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="da15d-157">在此裝置說明中，裝置控制物件會讀取指派給裝置樹狀結構中每個裝置的 UDNs。</span><span class="sxs-lookup"><span data-stu-id="da15d-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="da15d-158">您也可以使用 [**IUPnPRegistrar：： GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) 方法來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="da15d-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="da15d-159">當裝置主機需要服務物件的指標來執行特定服務時，它會在裝置控制物件上叫用 [**IUPnPDeviceControl：： GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="da15d-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="da15d-160">裝置主機會傳遞 UDN，以及它要求服務物件之服務的服務識別碼，以及該方法預期會傳回服務物件指標的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標位址。</span><span class="sxs-lookup"><span data-stu-id="da15d-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="da15d-161">UDN 參數是必要的，因為裝置控制物件會管理整個裝置樹狀結構的服務，包括嵌套的裝置。</span><span class="sxs-lookup"><span data-stu-id="da15d-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="da15d-162">如果裝置主機要求嵌套裝置， **GetServiceObject** 會使用 UDN 來識別該裝置。</span><span class="sxs-lookup"><span data-stu-id="da15d-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 