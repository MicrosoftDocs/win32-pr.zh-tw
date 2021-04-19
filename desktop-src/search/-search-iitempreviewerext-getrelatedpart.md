---
description: 取得要內嵌至輸出 MHTML 資料流程的相關主體部分。
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: IItemPreviewerExt：： GetRelatedPart 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972386"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="48825-103">IItemPreviewerExt：： GetRelatedPart 方法</span><span class="sxs-lookup"><span data-stu-id="48825-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="48825-104">取得要內嵌至輸出 MHTML 資料流程的相關主體部分。</span><span class="sxs-lookup"><span data-stu-id="48825-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="48825-105">語法</span><span class="sxs-lookup"><span data-stu-id="48825-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="48825-106">參數</span><span class="sxs-lookup"><span data-stu-id="48825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48825-107">*dwCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48825-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48825-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="48825-108">Type: **DWORD**</span></span>

<span data-ttu-id="48825-109">作業的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="48825-109">The context identifier for the operation.</span></span> <span data-ttu-id="48825-110">覆寫 **dwCoNtext** 預設值，將內容識別碼設定為您選擇的值。</span><span class="sxs-lookup"><span data-stu-id="48825-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="48825-111">*pwszProp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48825-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48825-112">類型： **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="48825-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="48825-113">作為 Unicode 字串之連結內容的屬性指標。</span><span class="sxs-lookup"><span data-stu-id="48825-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="48825-114">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48825-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48825-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="48825-115">Type: **DWORD**</span></span>

<span data-ttu-id="48825-116">不帶正負號的長整數值，其中包含相關主體部分以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="48825-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="48825-117">*pInfo* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="48825-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="48825-118">類型： \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="48825-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="48825-119">接收 [_ *LINKINFO* \*](-search-linkinfo.md)結構的指標，此結構的方法會傳回交易的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="48825-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="48825-120">*pInfo* 不得為 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="48825-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48825-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="48825-121">Return value</span></span>

<span data-ttu-id="48825-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48825-122">Type: **HRESULT**</span></span>

<span data-ttu-id="48825-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="48825-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48825-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="48825-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48825-125">備註</span><span class="sxs-lookup"><span data-stu-id="48825-125">Remarks</span></span>

<span data-ttu-id="48825-126">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="48825-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="48825-127">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="48825-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="48825-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="48825-128">Requirements</span></span>



| <span data-ttu-id="48825-129">需求</span><span class="sxs-lookup"><span data-stu-id="48825-129">Requirement</span></span> | <span data-ttu-id="48825-130">值</span><span class="sxs-lookup"><span data-stu-id="48825-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48825-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48825-131">Minimum supported client</span></span><br/> | <span data-ttu-id="48825-132">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48825-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48825-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48825-133">Minimum supported server</span></span><br/> | <span data-ttu-id="48825-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48825-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48825-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="48825-135">Redistributable</span></span><br/>          | <span data-ttu-id="48825-136">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="48825-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="48825-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48825-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48825-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="48825-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




