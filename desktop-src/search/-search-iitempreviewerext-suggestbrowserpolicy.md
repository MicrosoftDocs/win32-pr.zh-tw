---
description: 建議要套用至瀏覽器的安全性原則。
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: IItemPreviewerExt：： SuggestBrowserPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468800"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="d6dae-103">IItemPreviewerExt：： SuggestBrowserPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="d6dae-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="d6dae-104">建議要套用至瀏覽器的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="d6dae-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dae-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6dae-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d6dae-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6dae-107">*dwCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6dae-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dae-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d6dae-108">Type: **DWORD**</span></span>

<span data-ttu-id="d6dae-109">作業的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6dae-109">The context identifier for the operation.</span></span> <span data-ttu-id="d6dae-110">覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。</span><span class="sxs-lookup"><span data-stu-id="d6dae-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="d6dae-111">*pdwFlags* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="d6dae-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dae-112">類型： \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="d6dae-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="d6dae-113">包含驗證檢查旗標之 DWORD 值的指標。</span><span class="sxs-lookup"><span data-stu-id="d6dae-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="d6dae-114">_ *BROWSERPOLICY 未 \_ 受信任的 \_ 內容*\* 旗標可停用任何可能的預覽執行腳本或 ActiveX。</span><span class="sxs-lookup"><span data-stu-id="d6dae-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="d6dae-115">參數 *pdwFlags* 不得為 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="d6dae-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6dae-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6dae-116">Return value</span></span>

<span data-ttu-id="d6dae-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6dae-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d6dae-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6dae-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6dae-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6dae-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6dae-120">備註</span><span class="sxs-lookup"><span data-stu-id="d6dae-120">Remarks</span></span>

<span data-ttu-id="d6dae-121">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="d6dae-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d6dae-122">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="d6dae-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="d6dae-123">強烈建議您不要使用 **BROWSERPOLICY \_ 不受信任的 \_ 內容** 旗標，以停用任何可能的預覽功能來執行腳本或 ActiveX。</span><span class="sxs-lookup"><span data-stu-id="d6dae-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="d6dae-124">**IItemPreviewerExt：： SuggestBrowserPolicy** 方法可以傳回所預覽專案是否受信任的資訊。</span><span class="sxs-lookup"><span data-stu-id="d6dae-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="d6dae-125">這可讓預覽 trident 控制項執行腳本，甚至是 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="d6dae-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="d6dae-126">因為預覽程式通常會使用暫存檔案來產生預覽，所以這樣做可能會導致在本機電腦區域中出現未預期的腳本和程式碼執行。</span><span class="sxs-lookup"><span data-stu-id="d6dae-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dae-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6dae-127">Requirements</span></span>



| <span data-ttu-id="d6dae-128">需求</span><span class="sxs-lookup"><span data-stu-id="d6dae-128">Requirement</span></span> | <span data-ttu-id="d6dae-129">值</span><span class="sxs-lookup"><span data-stu-id="d6dae-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6dae-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6dae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dae-131">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6dae-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6dae-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6dae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dae-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6dae-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6dae-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d6dae-134">Redistributable</span></span><br/>          | <span data-ttu-id="d6dae-135">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="d6dae-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d6dae-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6dae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dae-137">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="d6dae-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




