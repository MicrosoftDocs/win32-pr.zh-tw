---
title: 透過 IWMDMDevice3 取得格式功能
description: 在支援 IWMDMDevice3 的裝置上取得格式功能
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Media 裝置管理員，裝置功能
- 裝置管理員，裝置功能
- 程式設計指南，裝置功能
- 桌面應用程式，裝置功能
- 建立 Windows Media 裝置管理員應用程式，裝置功能
- 將檔案寫入裝置、裝置功能
- IWMDMDevice3 方法
- Windows Media 裝置管理員，IWMDMDevice3 方法
- 裝置管理員，IWMDMDevice3 方法
- 程式設計手冊，IWMDMDevice3 方法
- 桌面應用程式，IWMDMDevice3 方法
- 建立 Windows Media 裝置管理員應用程式，IWMDMDevice3 方法
- 將檔案寫入裝置，IWMDMDevice3 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104022892"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="d93a8-116">透過 IWMDMDevice3 取得格式功能</span><span class="sxs-lookup"><span data-stu-id="d93a8-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="d93a8-117">[**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) 是詢問裝置所支援之格式的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="d93a8-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="d93a8-118">下列步驟示範如何使用此方法來查詢裝置的格式功能：</span><span class="sxs-lookup"><span data-stu-id="d93a8-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="d93a8-119">應用程式必須決定裝置支援的格式以及感興趣的格式。</span><span class="sxs-lookup"><span data-stu-id="d93a8-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="d93a8-120">若要這樣做，應用程式可以呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)來要求裝置所支援的格式清單。</span><span class="sxs-lookup"><span data-stu-id="d93a8-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="d93a8-121">應用程式會迴圈執行所有支援的格式，並針對特定格式要求裝置的格式功能 (例如 WMA 或 WMV) ，方法是呼叫 **IWMDMDevice3：： GetFormatCapability** ，並使用 [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) 列舉來指定格式。</span><span class="sxs-lookup"><span data-stu-id="d93a8-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="d93a8-122">這個方法會捕獲 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d93a8-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="d93a8-123">使用已抓取之 **WMDM \_ 格式 \_ 功能** 結構中所有的 [**WMDM \_ \_ 配置**](wmdm-prop-config.md)設定結構來執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="d93a8-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="d93a8-124">每個 WMDM 屬性設定結構都會保存具有支援值的一組屬性，代表該格式的一項設定。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="d93a8-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="d93a8-125">每個設定都有喜好設定數位，其中較低的數位表示裝置的喜好設定較大。</span><span class="sxs-lookup"><span data-stu-id="d93a8-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="d93a8-126">在抓取的 **WMDM \_ \_ 配置** 設定中，對所有 [**WMDM 的配置 \_ \_ DESC**](wmdm-prop-desc.md)結構執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="d93a8-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="d93a8-127">每個 **WMDM 屬性 \_ \_ DESC** 都包含一份支援的屬性/值組清單。</span><span class="sxs-lookup"><span data-stu-id="d93a8-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="d93a8-128">從 WMDM 的屬性 **\_ \_ DESC** 結構中取出屬性名稱和值。</span><span class="sxs-lookup"><span data-stu-id="d93a8-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="d93a8-129">屬性包含位元速率、編解碼器和框架大小。</span><span class="sxs-lookup"><span data-stu-id="d93a8-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="d93a8-130">屬性名稱定義于 mswmdm .h 標頭檔中;這些常數的其中一個清單會在 [中繼資料常數](metadata-constants.md)中提供。</span><span class="sxs-lookup"><span data-stu-id="d93a8-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="d93a8-131">可能有三種類型的屬性值：</span><span class="sxs-lookup"><span data-stu-id="d93a8-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="d93a8-132">單一值，WMDM 列舉會將 \_ \_ \_ 有效值 \_ \_ 為有效值，表示支援此屬性的任何值。</span><span class="sxs-lookup"><span data-stu-id="d93a8-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="d93a8-133">值的範圍，以最大值、最小值和間隔來定義。</span><span class="sxs-lookup"><span data-stu-id="d93a8-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="d93a8-134">離散值的清單。</span><span class="sxs-lookup"><span data-stu-id="d93a8-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="d93a8-135">清除儲存的值。</span><span class="sxs-lookup"><span data-stu-id="d93a8-135">Clear the stored values.</span></span> <span data-ttu-id="d93a8-136">這些值的記憶體是由 Windows Media 裝置管理員配置;您的裝置負責釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="d93a8-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="d93a8-137">本主題結尾會說明如何進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="d93a8-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="d93a8-138">當回應 **GetFormatCapability** 時，裝置可以 \_ \_ \_ \_ \_ 針對 **WMDM \_ 格式 \_ 功能報告 WMDM 列舉的有效值。WMDM \_ \_ 配置設定。WMDM \_ \_ 的： DESC。ValidValuesForm** 可支援任何位速率、通道等值的值。</span><span class="sxs-lookup"><span data-stu-id="d93a8-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="d93a8-139">不過，您應該小心處理此宣告，因為裝置有時可以報告任何值的支援，事實上它們並不支援所有的位元速率或映射大小。</span><span class="sxs-lookup"><span data-stu-id="d93a8-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="d93a8-140">您可以考慮讓應用程式將極大型或高位速率的檔案轉碼至較小的版本，或較少的記憶體和 CPU 密集的版本，將它們傳送給預定播放這些檔案的裝置。</span><span class="sxs-lookup"><span data-stu-id="d93a8-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="d93a8-141">下列 c + + 函式顯示如何要求特定格式的裝置格式支援。</span><span class="sxs-lookup"><span data-stu-id="d93a8-141">The following C++ function shows how to request device format support for a specific format.</span></span>


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



<span data-ttu-id="d93a8-142">**清除配置的記憶體**</span><span class="sxs-lookup"><span data-stu-id="d93a8-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="d93a8-143">從裝置上取出格式功能之後，應用程式必須釋放配置用來保存描述的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d93a8-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="d93a8-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) 和 [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) 具有簡單結構的陣列，只要呼叫 **CoTaskMemFree** 與陣列即可清除。</span><span class="sxs-lookup"><span data-stu-id="d93a8-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="d93a8-145">不過， **GetFormatCapability** 有一個更複雜的資料結構，其具有動態配置的記憶體，必須透過迴圈所有元素並個別釋放它們來清除。</span><span class="sxs-lookup"><span data-stu-id="d93a8-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="d93a8-146">下列 c + + 程式碼顯示應用程式如何釋放配置給 **WMDM \_ 格式 \_ 功能** 結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d93a8-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



<span data-ttu-id="d93a8-147">**查詢所有支援的格式**</span><span class="sxs-lookup"><span data-stu-id="d93a8-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="d93a8-148">一般而言，應用程式會查詢特定格式的裝置，因為它有興趣將特定檔案傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="d93a8-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="d93a8-149">但是，如果您想要查詢應用程式的所有支援格式，您可以呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ，並傳入 g \_ wszWMDMFormatsSupported 以取得完整清單。</span><span class="sxs-lookup"><span data-stu-id="d93a8-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="d93a8-150">如果裝置只會傳回一個元素，WMDM \_ FORMATCODE \_ 未定義，這通常表示裝置不支援格式代碼。</span><span class="sxs-lookup"><span data-stu-id="d93a8-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="d93a8-151">使用 WMDM \_ FORMATCODE 未定義呼叫 GetFormatCapability 可能會抓取 \_ 功能，但這些屬性可能是相當泛型 (例如名稱、檔案大小、上次修改日期等) 。</span><span class="sxs-lookup"><span data-stu-id="d93a8-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="d93a8-152">下列步驟說明如何查詢所有支援的格式清單：</span><span class="sxs-lookup"><span data-stu-id="d93a8-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="d93a8-153">要求透過呼叫 **IWMDMDevice3：： GetProperty** 並傳入 g wszWMDMFormatsSupported 所支援的所有格式代碼清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d93a8-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="d93a8-154">這會傳回 **PROPVARIANT** ，其中包含支援格式的 **SAFEARRAY** 。</span><span class="sxs-lookup"><span data-stu-id="d93a8-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="d93a8-155">藉由呼叫 **SafeArrayGetElement** 來迴圈執行元素。</span><span class="sxs-lookup"><span data-stu-id="d93a8-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="d93a8-156">每個元素都是 **WMDM \_ FORMATCODE** 列舉。</span><span class="sxs-lookup"><span data-stu-id="d93a8-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="d93a8-157">要求每個格式的功能，並在完成後釋出每個 **WMDM \_ 格式 \_ 功能** 元素的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d93a8-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="d93a8-158">藉由呼叫 **PropVariantClear**，清除在步驟1中取出的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="d93a8-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="d93a8-159">下列 c + + 範例程式碼會抓取裝置支援的格式清單。</span><span class="sxs-lookup"><span data-stu-id="d93a8-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d93a8-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="d93a8-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93a8-161">**探索裝置格式功能**</span><span class="sxs-lookup"><span data-stu-id="d93a8-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




