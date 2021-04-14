---
description: 建立列舉值物件，並將指標傳回到其 IEnumWiaItem2 介面，以取得 Windows 影像取得之 IWiaItem2 樹狀目錄中的專案（ (WIA) 2.0 裝置）的資料夾。
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2：： EnumChildItems 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469120"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="d6a75-103">IWiaItem2：： EnumChildItems 方法</span><span class="sxs-lookup"><span data-stu-id="d6a75-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="d6a75-104">建立列舉值物件，並將指標傳回到其 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面，以取得 Windows 影像取得之 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀目錄中的專案（ (WIA) 2.0 裝置）的資料夾。</span><span class="sxs-lookup"><span data-stu-id="d6a75-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a75-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6a75-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="d6a75-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6a75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a75-107">*pCategoryGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a75-108">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="d6a75-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="d6a75-109">指定要列舉其子節點的分類指標。</span><span class="sxs-lookup"><span data-stu-id="d6a75-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="d6a75-110">如果 _ \* Null \* \*，則會列舉所有的子節點。</span><span class="sxs-lookup"><span data-stu-id="d6a75-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="d6a75-111">*ppIEnumWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a75-112">類型： **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d6a75-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="d6a75-113">接收這個方法所建立之 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="d6a75-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a75-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6a75-114">Return value</span></span>

<span data-ttu-id="d6a75-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-115">Type: **HRESULT**</span></span>

<span data-ttu-id="d6a75-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6a75-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6a75-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6a75-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a75-118">備註</span><span class="sxs-lookup"><span data-stu-id="d6a75-118">Remarks</span></span>

<span data-ttu-id="d6a75-119">WIA 2.0 執行時間系統會將每個 WIA 2.0 硬體裝置表示為 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="d6a75-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="d6a75-120">**IWiaItem2：： EnumChildItems** 方法可讓應用程式列舉目前專案中的子專案。</span><span class="sxs-lookup"><span data-stu-id="d6a75-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="d6a75-121">不過，它只能套用至資料夾的專案。</span><span class="sxs-lookup"><span data-stu-id="d6a75-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="d6a75-122">如果資料夾不是空的，它就會包含 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的子樹。</span><span class="sxs-lookup"><span data-stu-id="d6a75-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="d6a75-123">**IWiaItem2：： EnumChildItems** 方法會列舉資料夾中包含的所有專案。</span><span class="sxs-lookup"><span data-stu-id="d6a75-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="d6a75-124">它會在 *ppIEnumWiaItem2* 參數中儲存列舉值的指標。</span><span class="sxs-lookup"><span data-stu-id="d6a75-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="d6a75-125">應用程式會使用列舉值指標來執行物件的子專案的列舉。</span><span class="sxs-lookup"><span data-stu-id="d6a75-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="d6a75-126">應用程式必須在透過 *ppIEnumWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="d6a75-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a75-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6a75-127">Requirements</span></span>



| <span data-ttu-id="d6a75-128">需求</span><span class="sxs-lookup"><span data-stu-id="d6a75-128">Requirement</span></span> | <span data-ttu-id="d6a75-129">值</span><span class="sxs-lookup"><span data-stu-id="d6a75-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a75-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6a75-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a75-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6a75-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6a75-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a75-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6a75-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d6a75-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a75-135"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="d6a75-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6a75-136">Idl</span><span class="sxs-lookup"><span data-stu-id="d6a75-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6a75-137"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6a75-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
