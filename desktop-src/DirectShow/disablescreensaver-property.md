---
description: DVDAdm. DisableScreenSaver 屬性會開啟或關閉系統螢幕保護裝置。
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: DisableScreenSaver 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845807"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="6f36f-103">DisableScreenSaver 屬性</span><span class="sxs-lookup"><span data-stu-id="6f36f-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="6f36f-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="6f36f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6f36f-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6f36f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6f36f-106">屬性會開啟 `DVDAdm.DisableScreenSaver` 或關閉系統螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6f36f-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="6f36f-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f36f-107">Return Value</span></span>

<span data-ttu-id="6f36f-108">傳回布林值，指出是否停用 DVD 播放機應用程式的系統螢幕保護裝置設定;true 表示設定已停用。</span><span class="sxs-lookup"><span data-stu-id="6f36f-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f36f-109">備註</span><span class="sxs-lookup"><span data-stu-id="6f36f-109">Remarks</span></span>

<span data-ttu-id="6f36f-110">此屬性是讀取/寫入，預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="6f36f-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="6f36f-111">在觀看 DVD-Video 光碟時，使用者通常不會在長時間內使用滑鼠或鍵盤。</span><span class="sxs-lookup"><span data-stu-id="6f36f-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="6f36f-112">因此，MSWebDVD ActiveX®控制項依預設會停用系統螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6f36f-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="6f36f-113">Object</span><span class="sxs-lookup"><span data-stu-id="6f36f-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="6f36f-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f36f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f36f-115">**RestoreScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="6f36f-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="6f36f-116">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="6f36f-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



