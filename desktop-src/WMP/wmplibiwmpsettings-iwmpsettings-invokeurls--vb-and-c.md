---
title: IWMPSettings invokeURLs 屬性
description: InvokeURLs 屬性會取得或設定值，指出 URL 事件是否應該啟動網頁瀏覽器。
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- invokeURLs 屬性 Windows Media Player
- invokeURLs 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，invokeURLs 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978531"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="cae50-106">IWMPSettings：： invokeURLs 屬性</span><span class="sxs-lookup"><span data-stu-id="cae50-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="cae50-107">**InvokeURLs** 屬性會取得或設定值，指出 URL 事件是否應該啟動網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="cae50-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae50-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae50-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="cae50-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="cae50-109">Property value</span></span>

<span data-ttu-id="cae50-110">System.string **值，** 指出 URL 事件是否應啟動網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="cae50-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="cae50-111">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="cae50-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae50-112">備註</span><span class="sxs-lookup"><span data-stu-id="cae50-112">Remarks</span></span>

<span data-ttu-id="cae50-113">數位媒體檔案和資料流程可以包含 URL 指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="cae50-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="cae50-114">將 URL 指令碼命令傳送給 Windows Media Player 控制項時，會先將它傳遞給 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件處理常式，而不論 **invokeURLs** 所抓取的值為何。</span><span class="sxs-lookup"><span data-stu-id="cae50-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="cae50-115">**\_ WMPOCXEvents \_ ScriptCommandEvent** 結束之後，Windows Media Player 會檢查 **invokeURLs** ，以判斷是否要使用 URL 啟動預設的網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="cae50-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="cae50-116">您可以選擇性地顯示 Url，方法是在 **\_ WMPOCXEvents \_ ScriptCommandEvent** 中進行檢查，並視需要設定 **invokeURLs** 。</span><span class="sxs-lookup"><span data-stu-id="cae50-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae50-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cae50-117">Requirements</span></span>



| <span data-ttu-id="cae50-118">需求</span><span class="sxs-lookup"><span data-stu-id="cae50-118">Requirement</span></span> | <span data-ttu-id="cae50-119">值</span><span class="sxs-lookup"><span data-stu-id="cae50-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae50-120">版本</span><span class="sxs-lookup"><span data-stu-id="cae50-120">Version</span></span><br/>   | <span data-ttu-id="cae50-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="cae50-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cae50-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="cae50-122">Namespace</span></span><br/> | <span data-ttu-id="cae50-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cae50-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cae50-124">組件</span><span class="sxs-lookup"><span data-stu-id="cae50-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cae50-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="cae50-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae50-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cae50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae50-127">**AxWindowsMediaPlayer ScriptCommand 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cae50-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="cae50-128">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="cae50-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





