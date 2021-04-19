---
description: 建立新的子專案。 將 IWiaItem2 物件新增至裝置的 IWiaItem2 樹狀目錄。
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2：： CreateChildItem 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983502"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="34a34-104">IWiaItem2：： CreateChildItem 方法</span><span class="sxs-lookup"><span data-stu-id="34a34-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="34a34-105">建立新的子專案。</span><span class="sxs-lookup"><span data-stu-id="34a34-105">Create a new child item.</span></span> <span data-ttu-id="34a34-106">將 [**IWiaItem2**](-wia-iwiaitem2.md) 物件新增至裝置的 **IWiaItem2** 樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="34a34-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a34-107">語法</span><span class="sxs-lookup"><span data-stu-id="34a34-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="34a34-108">參數</span><span class="sxs-lookup"><span data-stu-id="34a34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a34-109">*lItemFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34a34-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a34-110">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="34a34-110">Type: **LONG**</span></span>

<span data-ttu-id="34a34-111">指定 WIA 2.0 專案類型。</span><span class="sxs-lookup"><span data-stu-id="34a34-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="34a34-112">請參閱 [**WIA 專案類型旗標**](-wia-wia-item-type-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="34a34-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="34a34-113">*lCreationFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34a34-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a34-114">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="34a34-114">Type: **LONG**</span></span>

<span data-ttu-id="34a34-115">指定如何建立新專案。</span><span class="sxs-lookup"><span data-stu-id="34a34-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="34a34-116"><span id="0"></span>**0** (0) </span><span class="sxs-lookup"><span data-stu-id="34a34-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="34a34-117">設定子系屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="34a34-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="34a34-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**複製 \_父 \_ 屬性 \_ 值** (0x40000000) </span><span class="sxs-lookup"><span data-stu-id="34a34-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="34a34-119">從父系複製所有讀取/寫入屬性的值。</span><span class="sxs-lookup"><span data-stu-id="34a34-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34a34-120">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34a34-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a34-121">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="34a34-121">Type: **BSTR**</span></span>

<span data-ttu-id="34a34-122">指定專案名稱。</span><span class="sxs-lookup"><span data-stu-id="34a34-122">Specifies the item name.</span></span> <span data-ttu-id="34a34-123">這個名稱會附加至父專案名稱的結尾，以產生完整的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="34a34-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="34a34-124">*ppIWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="34a34-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a34-125">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="34a34-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="34a34-126">接收 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址，此介面會設定 **IWiaItem2：： CreateChildItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="34a34-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a34-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="34a34-127">Return value</span></span>

<span data-ttu-id="34a34-128">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="34a34-128">Type: **HRESULT**</span></span>

<span data-ttu-id="34a34-129">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="34a34-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34a34-130">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="34a34-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a34-131">備註</span><span class="sxs-lookup"><span data-stu-id="34a34-131">Remarks</span></span>

<span data-ttu-id="34a34-132">某些 WIA 2.0 硬體裝置可讓應用程式在代表裝置的 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀結構中建立新專案。</span><span class="sxs-lookup"><span data-stu-id="34a34-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="34a34-133">應用程式必須測試裝置，才能查看是否支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="34a34-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="34a34-134">使用 IEnumWIA \_ DEV \_ CAPS 介面來列舉目前裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="34a34-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="34a34-135">如果裝置允許在 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀結構中建立新專案，則叫用 **IWiaItem2：： CreateChildItem** 會建立新的 **IWiaItem2** 物件，該物件為目前節點的子系。</span><span class="sxs-lookup"><span data-stu-id="34a34-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="34a34-136">它會透過 *ppIWiaItem2* 參數，將新節點的指標傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="34a34-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="34a34-137">應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="34a34-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="34a34-138">如果 *lCreationFlags* 是複製 \_ 父 \_ 屬性 \_ 值， *而 lItemFlags* 為零，則函數會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="34a34-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a34-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="34a34-139">Requirements</span></span>



| <span data-ttu-id="34a34-140">需求</span><span class="sxs-lookup"><span data-stu-id="34a34-140">Requirement</span></span> | <span data-ttu-id="34a34-141">值</span><span class="sxs-lookup"><span data-stu-id="34a34-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34a34-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34a34-142">Minimum supported client</span></span><br/> | <span data-ttu-id="34a34-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34a34-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34a34-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34a34-144">Minimum supported server</span></span><br/> | <span data-ttu-id="34a34-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34a34-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34a34-146">標頭</span><span class="sxs-lookup"><span data-stu-id="34a34-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a34-147"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="34a34-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="34a34-148">Idl</span><span class="sxs-lookup"><span data-stu-id="34a34-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34a34-149"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="34a34-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
