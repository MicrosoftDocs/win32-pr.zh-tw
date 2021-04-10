---
title: ShowMessageAction Title 屬性
description: 針對腳本，取得或設定訊息方塊的標題。
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Title 屬性工作排程器
- Title 屬性工作排程器，ShowMessageAction 物件
- ShowMessageAction 物件工作排程器、Title 屬性
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685683"
---
# <a name="showmessageactiontitle-property"></a><span data-ttu-id="3f676-106">ShowMessageAction Title 屬性</span><span class="sxs-lookup"><span data-stu-id="3f676-106">ShowMessageAction.Title property</span></span>

<span data-ttu-id="3f676-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="3f676-107">\[This object is no longer supported.</span></span> <span data-ttu-id="3f676-108">您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80)) ，在使用者會話中顯示訊息。\]</span><span class="sxs-lookup"><span data-stu-id="3f676-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="3f676-109">針對腳本，取得或設定訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="3f676-109">For scripting, gets or sets the title of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f676-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f676-110">Syntax</span></span>


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a><span data-ttu-id="3f676-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="3f676-111">Property value</span></span>

<span data-ttu-id="3f676-112">訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="3f676-112">The title of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f676-113">備註</span><span class="sxs-lookup"><span data-stu-id="3f676-113">Remarks</span></span>

<span data-ttu-id="3f676-114">參數化字串可以在訊息方塊的標題文字中使用。</span><span class="sxs-lookup"><span data-stu-id="3f676-114">Parameterized strings can be used in the title text of the message box.</span></span> <span data-ttu-id="3f676-115">如需詳細資訊，請參閱 [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)中的範例一節。</span><span class="sxs-lookup"><span data-stu-id="3f676-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="3f676-116">設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。</span><span class="sxs-lookup"><span data-stu-id="3f676-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="3f676-117">特製化的字串會用來參考資源檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="3f676-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="3f676-118">字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f676-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="3f676-119">例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="3f676-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f676-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f676-120">Requirements</span></span>



| <span data-ttu-id="3f676-121">需求</span><span class="sxs-lookup"><span data-stu-id="3f676-121">Requirement</span></span> | <span data-ttu-id="3f676-122">值</span><span class="sxs-lookup"><span data-stu-id="3f676-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f676-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f676-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3f676-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f676-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f676-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f676-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3f676-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f676-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f676-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3f676-127">End of client support</span></span><br/>    | <span data-ttu-id="3f676-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f676-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="3f676-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="3f676-129">End of server support</span></span><br/>    | <span data-ttu-id="3f676-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f676-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3f676-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3f676-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f676-132"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f676-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f676-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3f676-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f676-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f676-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f676-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f676-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f676-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="3f676-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

