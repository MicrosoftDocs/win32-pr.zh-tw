---
title: AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件
description: 當資料夾監控操作變更狀態時，就會發生 FolderScanStateChange 事件。
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989252"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c8a72-104">AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="c8a72-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c8a72-105">當資料夾監控操作變更狀態時，就會發生 FolderScanStateChange 事件。</span><span class="sxs-lookup"><span data-stu-id="c8a72-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="c8a72-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="c8a72-106">Event Data</span></span>

<span data-ttu-id="c8a72-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ FolderScanStateChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="c8a72-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="c8a72-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ FolderScanStateChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c8a72-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c8a72-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c8a72-109">Property</span></span> | <span data-ttu-id="c8a72-110">描述</span><span class="sxs-lookup"><span data-stu-id="c8a72-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a72-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="c8a72-111">wmpfss</span></span>   | <span data-ttu-id="c8a72-112">WMPLib，表示新狀態的 WMPFolderScanStateThe 列舉值。</span><span class="sxs-lookup"><span data-stu-id="c8a72-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8a72-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8a72-113">Requirements</span></span>



| <span data-ttu-id="c8a72-114">需求</span><span class="sxs-lookup"><span data-stu-id="c8a72-114">Requirement</span></span> | <span data-ttu-id="c8a72-115">值</span><span class="sxs-lookup"><span data-stu-id="c8a72-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a72-116">版本</span><span class="sxs-lookup"><span data-stu-id="c8a72-116">Version</span></span><br/>   | <span data-ttu-id="c8a72-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="c8a72-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="c8a72-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8a72-118">Namespace</span></span><br/> | <span data-ttu-id="c8a72-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c8a72-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c8a72-120">組件</span><span class="sxs-lookup"><span data-stu-id="c8a72-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c8a72-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c8a72-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a72-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8a72-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a72-123">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c8a72-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8a72-124">**WMPFolderScanState**</span><span class="sxs-lookup"><span data-stu-id="c8a72-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





