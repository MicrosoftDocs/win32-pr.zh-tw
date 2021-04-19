---
title: WMDM_PROP_DESC 結構
description: WMDM 屬性 \_ \_ DESC 結構描述特定屬性設定中的有效值。
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984822"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="5cd82-104">WMDM \_ \_ 架構 DESC 結構</span><span class="sxs-lookup"><span data-stu-id="5cd82-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="5cd82-105">**WMDM 屬性 \_ \_ DESC** 結構描述特定屬性設定中的有效值。</span><span class="sxs-lookup"><span data-stu-id="5cd82-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd82-106">語法</span><span class="sxs-lookup"><span data-stu-id="5cd82-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="5cd82-107">成員</span><span class="sxs-lookup"><span data-stu-id="5cd82-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5cd82-108">**pwszPropName**</span><span class="sxs-lookup"><span data-stu-id="5cd82-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="5cd82-109">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cd82-109">Name of the property.</span></span> <span data-ttu-id="5cd82-110">應用程式必須在使用它完成時釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="5cd82-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="5cd82-111">**ValidValuesForm**</span><span class="sxs-lookup"><span data-stu-id="5cd82-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="5cd82-112">WMDM 列舉會描述數值型別的 [**\_ \_ \_ 有效 \_ 值 \_ 形式**](wmdm-enum-prop-valid-values-form.md) 列舉值，例如範圍或清單。</span><span class="sxs-lookup"><span data-stu-id="5cd82-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="5cd82-113">此列舉的值會決定要使用的成員變數。</span><span class="sxs-lookup"><span data-stu-id="5cd82-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="5cd82-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="5cd82-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="5cd82-115">在特定屬性設定中保存屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="5cd82-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="5cd82-116">這個成員有三個專案的其中一個：列舉值 WMDM ENUM 會將 \_ \_ 有效值的 \_ \_ 值 \_ 為 ANY、member **ValidValuesRange** 或 member **EnumeratedValidValues**。</span><span class="sxs-lookup"><span data-stu-id="5cd82-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="5cd82-117">值或成員會以 **ValidValuesForm** 表示。</span><span class="sxs-lookup"><span data-stu-id="5cd82-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="5cd82-118">**ValidValuesRange**</span><span class="sxs-lookup"><span data-stu-id="5cd82-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="5cd82-119">包含有效值範圍的 [**WMDM 架構 \_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5cd82-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="5cd82-120">只有當 **ValidValuesForm** 設定為 WMDM \_ 列舉 \_ 值的 \_ 有效值 \_ \_ 範圍時，才會出現此情況。</span><span class="sxs-lookup"><span data-stu-id="5cd82-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="5cd82-121">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5cd82-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5cd82-122">**EnumeratedValidValues**</span><span class="sxs-lookup"><span data-stu-id="5cd82-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="5cd82-123">[**WMDM 的 \_ 規定 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)結構，其中包含有效值的列舉集合。</span><span class="sxs-lookup"><span data-stu-id="5cd82-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="5cd82-124">只有當 **ValidValuesForm** 設定為 WMDM \_ enum 的 \_ \_ VALID \_ 值 \_ 列舉時，才會出現這種情況。</span><span class="sxs-lookup"><span data-stu-id="5cd82-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="5cd82-125">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5cd82-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cd82-126">備註</span><span class="sxs-lookup"><span data-stu-id="5cd82-126">Remarks</span></span>

<span data-ttu-id="5cd82-127">**WMDM 屬性 \_ \_ DESC** 結構包含屬性描述，其中包含屬性名稱及其在特定設定中的有效值。</span><span class="sxs-lookup"><span data-stu-id="5cd82-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="5cd82-128">需要呼叫端才能釋放 **ValidValuesRange** 或 **EnumeratedValues** 所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5cd82-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="5cd82-129">如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。</span><span class="sxs-lookup"><span data-stu-id="5cd82-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd82-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cd82-130">Requirements</span></span>



| <span data-ttu-id="5cd82-131">需求</span><span class="sxs-lookup"><span data-stu-id="5cd82-131">Requirement</span></span> | <span data-ttu-id="5cd82-132">值</span><span class="sxs-lookup"><span data-stu-id="5cd82-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd82-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5cd82-133">Header</span></span><br/> | <dl> <span data-ttu-id="5cd82-134"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5cd82-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd82-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cd82-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd82-136">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="5cd82-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="5cd82-137">**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**</span><span class="sxs-lookup"><span data-stu-id="5cd82-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="5cd82-138">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="5cd82-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="5cd82-139">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="5cd82-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="5cd82-140">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="5cd82-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="5cd82-141">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="5cd82-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="5cd82-142">**結構**</span><span class="sxs-lookup"><span data-stu-id="5cd82-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





