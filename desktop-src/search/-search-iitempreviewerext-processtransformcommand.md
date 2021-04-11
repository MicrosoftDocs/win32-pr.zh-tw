---
description: 允許處理在預覽範本中遇到的轉換命令。
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt：:P rocessTransformCommand 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847818"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="bced4-103">IItemPreviewerExt：:P rocessTransformCommand 方法</span><span class="sxs-lookup"><span data-stu-id="bced4-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="bced4-104">允許處理在預覽範本中遇到的轉換命令。</span><span class="sxs-lookup"><span data-stu-id="bced4-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="bced4-105">語法</span><span class="sxs-lookup"><span data-stu-id="bced4-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="bced4-106">參數</span><span class="sxs-lookup"><span data-stu-id="bced4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bced4-107">*dwCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bced4-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bced4-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bced4-108">Type: **DWORD**</span></span>

<span data-ttu-id="bced4-109">作業的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="bced4-109">The context identifier for the operation.</span></span> <span data-ttu-id="bced4-110">覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。</span><span class="sxs-lookup"><span data-stu-id="bced4-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="bced4-111">*pwszName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bced4-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bced4-112">類型： **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="bced4-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="bced4-113">轉換命令名稱的指標，作為 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="bced4-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="bced4-114">*pwszArg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bced4-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bced4-115">類型： **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="bced4-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="bced4-116">引數的指標，作為 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="bced4-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="bced4-117">*pvarResult* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="bced4-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bced4-118">類型： \**VARIANT \** _</span><span class="sxs-lookup"><span data-stu-id="bced4-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="bced4-119">結果 variant 的指標。</span><span class="sxs-lookup"><span data-stu-id="bced4-119">A pointer to the result variant.</span></span> <span data-ttu-id="bced4-120">_pvarResult \* 不得為 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="bced4-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bced4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="bced4-121">Return value</span></span>

<span data-ttu-id="bced4-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bced4-122">Type: **HRESULT**</span></span>

<span data-ttu-id="bced4-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bced4-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bced4-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bced4-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bced4-125">備註</span><span class="sxs-lookup"><span data-stu-id="bced4-125">Remarks</span></span>

<span data-ttu-id="bced4-126">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="bced4-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="bced4-127">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="bced4-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bced4-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bced4-128">Requirements</span></span>



| <span data-ttu-id="bced4-129">需求</span><span class="sxs-lookup"><span data-stu-id="bced4-129">Requirement</span></span> | <span data-ttu-id="bced4-130">值</span><span class="sxs-lookup"><span data-stu-id="bced4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bced4-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bced4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bced4-132">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bced4-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bced4-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bced4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bced4-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bced4-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bced4-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bced4-135">Redistributable</span></span><br/>          | <span data-ttu-id="bced4-136">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="bced4-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bced4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bced4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bced4-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="bced4-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




