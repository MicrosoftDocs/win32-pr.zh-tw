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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>透過 IWMDMDevice3 取得格式功能

[**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) 是詢問裝置所支援之格式的慣用方法。 下列步驟示範如何使用此方法來查詢裝置的格式功能：

1.  應用程式必須決定裝置支援的格式以及感興趣的格式。 若要這樣做，應用程式可以呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)來要求裝置所支援的格式清單。
2.  應用程式會迴圈執行所有支援的格式，並針對特定格式要求裝置的格式功能 (例如 WMA 或 WMV) ，方法是呼叫 **IWMDMDevice3：： GetFormatCapability** ，並使用 [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) 列舉來指定格式。 這個方法會捕獲 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md) 結構。
3.  使用已抓取之 **WMDM \_ 格式 \_ 功能** 結構中所有的 [**WMDM \_ \_ 配置**](wmdm-prop-config.md)設定結構來執行迴圈。 每個 WMDM 屬性設定結構都會保存具有支援值的一組屬性，代表該格式的一項設定。 **\_ \_** 每個設定都有喜好設定數位，其中較低的數位表示裝置的喜好設定較大。
4.  在抓取的 **WMDM \_ \_ 配置** 設定中，對所有 [**WMDM 的配置 \_ \_ DESC**](wmdm-prop-desc.md)結構執行迴圈。 每個 **WMDM 屬性 \_ \_ DESC** 都包含一份支援的屬性/值組清單。
5.  從 WMDM 的屬性 **\_ \_ DESC** 結構中取出屬性名稱和值。 屬性包含位元速率、編解碼器和框架大小。 屬性名稱定義于 mswmdm .h 標頭檔中;這些常數的其中一個清單會在 [中繼資料常數](metadata-constants.md)中提供。 可能有三種類型的屬性值：
    -   單一值，WMDM 列舉會將 \_ \_ \_ 有效值 \_ \_ 為有效值，表示支援此屬性的任何值。
    -   值的範圍，以最大值、最小值和間隔來定義。
    -   離散值的清單。
6.  清除儲存的值。 這些值的記憶體是由 Windows Media 裝置管理員配置;您的裝置負責釋放記憶體。 本主題結尾會說明如何進行這項操作。

當回應 **GetFormatCapability** 時，裝置可以 \_ \_ \_ \_ \_ 針對 **WMDM \_ 格式 \_ 功能報告 WMDM 列舉的有效值。WMDM \_ \_ 配置設定。WMDM \_ \_ 的： DESC。ValidValuesForm** 可支援任何位速率、通道等值的值。 不過，您應該小心處理此宣告，因為裝置有時可以報告任何值的支援，事實上它們並不支援所有的位元速率或映射大小。 您可以考慮讓應用程式將極大型或高位速率的檔案轉碼至較小的版本，或較少的記憶體和 CPU 密集的版本，將它們傳送給預定播放這些檔案的裝置。

下列 c + + 函式顯示如何要求特定格式的裝置格式支援。


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



**清除配置的記憶體**

從裝置上取出格式功能之後，應用程式必須釋放配置用來保存描述的記憶體。 [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) 和 [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) 具有簡單結構的陣列，只要呼叫 **CoTaskMemFree** 與陣列即可清除。 不過， **GetFormatCapability** 有一個更複雜的資料結構，其具有動態配置的記憶體，必須透過迴圈所有元素並個別釋放它們來清除。

下列 c + + 程式碼顯示應用程式如何釋放配置給 **WMDM \_ 格式 \_ 功能** 結構的記憶體。


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



**查詢所有支援的格式**

一般而言，應用程式會查詢特定格式的裝置，因為它有興趣將特定檔案傳送至裝置。 但是，如果您想要查詢應用程式的所有支援格式，您可以呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ，並傳入 g \_ wszWMDMFormatsSupported 以取得完整清單。

如果裝置只會傳回一個元素，WMDM \_ FORMATCODE \_ 未定義，這通常表示裝置不支援格式代碼。 使用 WMDM \_ FORMATCODE 未定義呼叫 GetFormatCapability 可能會抓取 \_ 功能，但這些屬性可能是相當泛型 (例如名稱、檔案大小、上次修改日期等) 。

下列步驟說明如何查詢所有支援的格式清單：

1.  要求透過呼叫 **IWMDMDevice3：： GetProperty** 並傳入 g wszWMDMFormatsSupported 所支援的所有格式代碼清單 \_ 。 這會傳回 **PROPVARIANT** ，其中包含支援格式的 **SAFEARRAY** 。
2.  藉由呼叫 **SafeArrayGetElement** 來迴圈執行元素。 每個元素都是 **WMDM \_ FORMATCODE** 列舉。
3.  要求每個格式的功能，並在完成後釋出每個 **WMDM \_ 格式 \_ 功能** 元素的記憶體。
4.  藉由呼叫 **PropVariantClear**，清除在步驟1中取出的 **PROPVARIANT** 。

下列 c + + 範例程式碼會抓取裝置支援的格式清單。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**探索裝置格式功能**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




