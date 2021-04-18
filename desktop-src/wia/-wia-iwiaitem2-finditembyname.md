---
description: 使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2：： FindItemByName 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971226"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="6ea61-103">IWiaItem2：： FindItemByName 方法</span><span class="sxs-lookup"><span data-stu-id="6ea61-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="6ea61-104">使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。</span><span class="sxs-lookup"><span data-stu-id="6ea61-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea61-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ea61-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="6ea61-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ea61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea61-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ea61-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea61-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="6ea61-108">Type: **LONG**</span></span>

<span data-ttu-id="6ea61-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="6ea61-109">Currently unused.</span></span> <span data-ttu-id="6ea61-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="6ea61-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ea61-111">*bstrFullItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ea61-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea61-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6ea61-112">Type: **BSTR**</span></span>

<span data-ttu-id="6ea61-113">指定要搜尋之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ea61-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="6ea61-114">*ppIWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ea61-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea61-115">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6ea61-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="6ea61-116">接收找到之專案的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標位址。</span><span class="sxs-lookup"><span data-stu-id="6ea61-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea61-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ea61-117">Return value</span></span>

<span data-ttu-id="6ea61-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ea61-118">Type: **HRESULT**</span></span>

<span data-ttu-id="6ea61-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6ea61-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ea61-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6ea61-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea61-121">備註</span><span class="sxs-lookup"><span data-stu-id="6ea61-121">Remarks</span></span>

<span data-ttu-id="6ea61-122">這個方法會使用名稱做為搜尋索引鍵，來搜尋目前專案的子專案樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="6ea61-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="6ea61-123">如果 **IWiaItem2：： FindItemByName** 找到 *bstrFullItemName* 所指定的專案，它會將指標的位址儲存至 *PpIWiaItem2* 參數中專案的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。</span><span class="sxs-lookup"><span data-stu-id="6ea61-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="6ea61-124">應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="6ea61-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea61-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ea61-125">Requirements</span></span>



| <span data-ttu-id="6ea61-126">需求</span><span class="sxs-lookup"><span data-stu-id="6ea61-126">Requirement</span></span> | <span data-ttu-id="6ea61-127">值</span><span class="sxs-lookup"><span data-stu-id="6ea61-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea61-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ea61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea61-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ea61-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ea61-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ea61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea61-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ea61-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ea61-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6ea61-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ea61-133"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="6ea61-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ea61-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6ea61-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ea61-135"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ea61-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
