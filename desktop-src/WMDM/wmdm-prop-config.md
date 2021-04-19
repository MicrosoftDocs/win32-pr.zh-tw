---
title: WMDM_PROP_CONFIG 結構
description: WMDM 屬性 \_ \_ 設定結構會針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。 此結構在 WMDM 屬性 DESC 結構的陣列中包含許多屬性 \_ 描述 \_ 。
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985939"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="65603-105">WMDM \_ \_ 配置設定結構</span><span class="sxs-lookup"><span data-stu-id="65603-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="65603-106">**WMDM 屬性 \_ 設定 \_** 結構會針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。</span><span class="sxs-lookup"><span data-stu-id="65603-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="65603-107">此結構在 [**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md) 結構的陣列中包含許多屬性描述。</span><span class="sxs-lookup"><span data-stu-id="65603-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="65603-108">語法</span><span class="sxs-lookup"><span data-stu-id="65603-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="65603-109">成員</span><span class="sxs-lookup"><span data-stu-id="65603-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="65603-110">**nPreference**</span><span class="sxs-lookup"><span data-stu-id="65603-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="65603-111">裝置針對此設定的喜好設定層級。</span><span class="sxs-lookup"><span data-stu-id="65603-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="65603-112">最小值表示最慣用的設定。</span><span class="sxs-lookup"><span data-stu-id="65603-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="65603-113">**nPropDesc**</span><span class="sxs-lookup"><span data-stu-id="65603-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="65603-114">此設定中包含的屬性描述數目。</span><span class="sxs-lookup"><span data-stu-id="65603-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="65603-115">針對指定的格式所支援的每個屬性都有一個屬性描述。</span><span class="sxs-lookup"><span data-stu-id="65603-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="65603-116">**pPropDesc**</span><span class="sxs-lookup"><span data-stu-id="65603-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="65603-117">[**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md)結構陣列的指標，其中包含屬性描述。</span><span class="sxs-lookup"><span data-stu-id="65603-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="65603-118">陣列的大小等於 **nPropDesc** 的值。</span><span class="sxs-lookup"><span data-stu-id="65603-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="65603-119">應用程式必須在完成時釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="65603-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65603-120">備註</span><span class="sxs-lookup"><span data-stu-id="65603-120">Remarks</span></span>

<span data-ttu-id="65603-121">[**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)針對特定格式所傳回的 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)結構包含一些屬性設定。</span><span class="sxs-lookup"><span data-stu-id="65603-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="65603-122">**WMDM \_配置 \_ 設定結構描述** 這些設定。</span><span class="sxs-lookup"><span data-stu-id="65603-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="65603-123">屬性設定會描述指定之格式支援的所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="65603-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="65603-124">單一設定中不同屬性的值彼此相容。</span><span class="sxs-lookup"><span data-stu-id="65603-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="65603-125">例如，對於音訊檔案，設定將包含有效的取樣率和有效的位元速率值，讓這些範例和位元速率的所有組合都可以在裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="65603-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="65603-126">需要呼叫端才能釋放 **pPropDesc** 所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="65603-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="65603-127">如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。</span><span class="sxs-lookup"><span data-stu-id="65603-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65603-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="65603-128">Requirements</span></span>



| <span data-ttu-id="65603-129">需求</span><span class="sxs-lookup"><span data-stu-id="65603-129">Requirement</span></span> | <span data-ttu-id="65603-130">值</span><span class="sxs-lookup"><span data-stu-id="65603-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65603-131">標頭</span><span class="sxs-lookup"><span data-stu-id="65603-131">Header</span></span><br/> | <dl> <span data-ttu-id="65603-132"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="65603-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65603-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65603-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65603-134">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="65603-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="65603-135">**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**</span><span class="sxs-lookup"><span data-stu-id="65603-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="65603-136">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="65603-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="65603-137">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="65603-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="65603-138">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="65603-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="65603-139">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="65603-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="65603-140">**結構**</span><span class="sxs-lookup"><span data-stu-id="65603-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





