---
title: RemoteWindowDisplayedAttribute 列舉
description: 與方法搭配使用，以指定事件的相關資訊。
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- RemoteWindowDisplayedAttribute 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967743"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a><span data-ttu-id="d8d29-104">RemoteWindowDisplayedAttribute 列舉</span><span class="sxs-lookup"><span data-stu-id="d8d29-104">RemoteWindowDisplayedAttribute enumeration</span></span>

<span data-ttu-id="d8d29-105">與方法搭配使用，以指定事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d8d29-105">Used with the method to specify information about the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d29-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8d29-106">Syntax</span></span>


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a><span data-ttu-id="d8d29-107">常數</span><span class="sxs-lookup"><span data-stu-id="d8d29-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d8d29-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span><span class="sxs-lookup"><span data-stu-id="d8d29-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8d29-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="d8d29-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d8d29-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span><span class="sxs-lookup"><span data-stu-id="d8d29-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span></span>
<span data-ttu-id="d8d29-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d8d29-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d8d29-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8d29-112">Requirements</span></span>



| <span data-ttu-id="d8d29-113">需求</span><span class="sxs-lookup"><span data-stu-id="d8d29-113">Requirement</span></span> | <span data-ttu-id="d8d29-114">值</span><span class="sxs-lookup"><span data-stu-id="d8d29-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d29-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8d29-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d29-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8d29-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="d8d29-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8d29-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d29-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8d29-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="d8d29-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d8d29-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8d29-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8d29-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d29-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8d29-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d29-122">**OnRemoteWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="d8d29-122">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





