---
description: 取得專案的類型資訊。
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2：： GetItemType 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690568"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="6319f-103">IWiaItem2：： GetItemType 方法</span><span class="sxs-lookup"><span data-stu-id="6319f-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="6319f-104">取得專案的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="6319f-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6319f-105">語法</span><span class="sxs-lookup"><span data-stu-id="6319f-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="6319f-106">參數</span><span class="sxs-lookup"><span data-stu-id="6319f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6319f-107">*pItemType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6319f-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6319f-108">類型： \**LONG \** _</span><span class="sxs-lookup"><span data-stu-id="6319f-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="6319f-109">接收 _ *LONG*\* 的指標，其中包含類型旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="6319f-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="6319f-110">請參閱 [**WIA 專案類型旗標**](-wia-wia-item-type-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6319f-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6319f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6319f-111">Return value</span></span>

<span data-ttu-id="6319f-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6319f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="6319f-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6319f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6319f-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6319f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6319f-115">備註</span><span class="sxs-lookup"><span data-stu-id="6319f-115">Remarks</span></span>

<span data-ttu-id="6319f-116">與 Windows 映像取得相關聯之物件的階層式樹狀結構中的每個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件 (WIA) 2.0 硬體裝置都有特定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6319f-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="6319f-117">專案物件代表資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="6319f-117">Item objects represent folders and files.</span></span> <span data-ttu-id="6319f-118">資料夾包含檔案物件。</span><span class="sxs-lookup"><span data-stu-id="6319f-118">Folders contain file objects.</span></span> <span data-ttu-id="6319f-119">檔案物件包含裝置所取得的資料，例如影像和聲音。</span><span class="sxs-lookup"><span data-stu-id="6319f-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="6319f-120">這個方法可讓應用程式在裝置的專案物件階層式樹狀結構中，識別任何專案的型別。</span><span class="sxs-lookup"><span data-stu-id="6319f-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="6319f-121">一個專案可以有一個以上的類型。</span><span class="sxs-lookup"><span data-stu-id="6319f-121">An item may have more than one type.</span></span> <span data-ttu-id="6319f-122">例如，代表音訊檔案的專案將會有 type 屬性 [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**。</span><span class="sxs-lookup"><span data-stu-id="6319f-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6319f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6319f-123">Requirements</span></span>



| <span data-ttu-id="6319f-124">需求</span><span class="sxs-lookup"><span data-stu-id="6319f-124">Requirement</span></span> | <span data-ttu-id="6319f-125">值</span><span class="sxs-lookup"><span data-stu-id="6319f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6319f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6319f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6319f-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6319f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6319f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6319f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6319f-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6319f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6319f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6319f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6319f-131"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="6319f-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6319f-132">Idl</span><span class="sxs-lookup"><span data-stu-id="6319f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6319f-133"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6319f-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




