---
title: WMDM_FORMAT_CAPABILITY 結構
description: WMDM \_ 格式 \_ 功能結構描述特定格式之裝置的功能。
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993961"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="8a5a8-104">WMDM \_ 格式 \_ 功能結構</span><span class="sxs-lookup"><span data-stu-id="8a5a8-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="8a5a8-105">**WMDM \_ 格式 \_ 功能** 結構描述特定格式之裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="8a5a8-106">此結構在 **WMDM \_ \_ 配置** 結構的陣列中包含一組屬性設定。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="8a5a8-107">每個屬性設定都代表一組相容的屬性值，這些屬性值橫跨指定格式支援的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="8a5a8-108">應用程式可以藉由呼叫 **IWMDMDevice3：： GetFormatCapability** 方法並傳入格式代碼，來取得此結構。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="8a5a8-109">如需格式代碼的清單，請參閱 [**WMDM \_ FORMATCODE**](wmdm-formatcode.md)。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5a8-110">語法</span><span class="sxs-lookup"><span data-stu-id="8a5a8-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="8a5a8-111">成員</span><span class="sxs-lookup"><span data-stu-id="8a5a8-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a5a8-112">**nPropConfig**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="8a5a8-113">**PConfigs** 陣列中的屬性設定數目。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="8a5a8-114">**pConfigs**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="8a5a8-115">[**WMDM \_ \_ 配置**](wmdm-prop-config.md)結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="8a5a8-116">陣列的大小等於 **nPropConfig** 的值。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a5a8-117">備註</span><span class="sxs-lookup"><span data-stu-id="8a5a8-117">Remarks</span></span>

<span data-ttu-id="8a5a8-118">**WMDM \_ 格式 \_ 功能** 結構提供了彈性的機制，可針對特定的格式來表示裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="8a5a8-119">如果內容是要由裝置轉譯 (例如，裝置) 要播放的音訊檔案，則內容屬性必須符合 **WMDM \_ 格式 \_ 功能** 結構中 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)所傳回的其中一個屬性設定。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="8a5a8-120">例如，對於音訊檔案，位元速率和取樣率必須符合其中一個傳回的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="8a5a8-121">呼叫端負責釋放配置給此結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="8a5a8-122">下列函式示範如何清除 **WMDM \_ 格式 \_ 功能** 結構。</span><span class="sxs-lookup"><span data-stu-id="8a5a8-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
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



## <a name="requirements"></a><span data-ttu-id="8a5a8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a5a8-123">Requirements</span></span>



| <span data-ttu-id="8a5a8-124">需求</span><span class="sxs-lookup"><span data-stu-id="8a5a8-124">Requirement</span></span> | <span data-ttu-id="8a5a8-125">值</span><span class="sxs-lookup"><span data-stu-id="8a5a8-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5a8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8a5a8-126">Header</span></span><br/> | <dl> <span data-ttu-id="8a5a8-127"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a5a8-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a5a8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a5a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5a8-129">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="8a5a8-130">**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="8a5a8-131">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="8a5a8-132">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="8a5a8-133">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="8a5a8-134">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="8a5a8-135">**結構**</span><span class="sxs-lookup"><span data-stu-id="8a5a8-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





