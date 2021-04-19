---
description: DVDAdm. RestoreScreenSaver 方法會還原系統螢幕保護裝置設定。
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: RestoreScreenSaver 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000039"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="b09d7-103">RestoreScreenSaver 方法</span><span class="sxs-lookup"><span data-stu-id="b09d7-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="b09d7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="b09d7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b09d7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b09d7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b09d7-106">`DVDAdm.RestoreScreenSaver`方法會還原系統螢幕保護裝置設定。</span><span class="sxs-lookup"><span data-stu-id="b09d7-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="b09d7-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="b09d7-107">Return Value</span></span>

<span data-ttu-id="b09d7-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b09d7-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b09d7-109">備註</span><span class="sxs-lookup"><span data-stu-id="b09d7-109">Remarks</span></span>

<span data-ttu-id="b09d7-110">一般而言，DVD 應用程式會在啟動時停用系統的螢幕保護裝置，方法是將 [ [**DisableScreenSaver**](disablescreensaver-property.md) ] 屬性設定為 [true]，然後在透過呼叫關閉 DVD 應用程式時重新啟用螢幕保護裝置 `RestoreScreenSaver` 。</span><span class="sxs-lookup"><span data-stu-id="b09d7-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="b09d7-111">如果應用程式未使用系統的螢幕保護裝置設定，則不需要呼叫這個方法或設定 **DisableScreenSaver** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b09d7-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="b09d7-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b09d7-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09d7-113">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="b09d7-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



