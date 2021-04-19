---
title: IWMPSettings defaultFrame 屬性
description: DefaultFrame 屬性會取得或設定用來顯示 AxWindowsMediaPlayer \_ WMPOCXEvents ScriptCommandEvent 事件中所接收之 URL 的框架名稱 \_ 。
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- defaultFrame 屬性 Windows Media Player
- defaultFrame 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，defaultFrame 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000712"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="d8df8-106">IWMPSettings：:d efaultFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="d8df8-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="d8df8-107">**DefaultFrame** 屬性會取得或設定用來顯示 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件中所接收之 URL 的框架名稱。</span><span class="sxs-lookup"><span data-stu-id="d8df8-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8df8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8df8-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="d8df8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8df8-109">Property value</span></span>

<span data-ttu-id="d8df8-110">**System.string** ，此為目標 **框架** 專案的 name 屬性值。</span><span class="sxs-lookup"><span data-stu-id="d8df8-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8df8-111">備註</span><span class="sxs-lookup"><span data-stu-id="d8df8-111">Remarks</span></span>

<span data-ttu-id="d8df8-112">如果在 **\_ WMPOCXEvents \_ ScriptCommandEvent** 事件本身中指定了目標框架，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d8df8-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="d8df8-113">使用 JAVA applet Netscape Navigator 時，會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d8df8-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="d8df8-114">在 Netscape Navigator 中，每個收到的 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，不論 **defaultFrame** 的值為何。</span><span class="sxs-lookup"><span data-stu-id="d8df8-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8df8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8df8-115">Requirements</span></span>



| <span data-ttu-id="d8df8-116">需求</span><span class="sxs-lookup"><span data-stu-id="d8df8-116">Requirement</span></span> | <span data-ttu-id="d8df8-117">值</span><span class="sxs-lookup"><span data-stu-id="d8df8-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8df8-118">版本</span><span class="sxs-lookup"><span data-stu-id="d8df8-118">Version</span></span><br/>   | <span data-ttu-id="d8df8-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d8df8-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d8df8-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8df8-120">Namespace</span></span><br/> | <span data-ttu-id="d8df8-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8df8-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d8df8-122">組件</span><span class="sxs-lookup"><span data-stu-id="d8df8-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8df8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d8df8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8df8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8df8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8df8-125">**AxWindowsMediaPlayer ScriptCommand 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8df8-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="d8df8-126">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8df8-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





