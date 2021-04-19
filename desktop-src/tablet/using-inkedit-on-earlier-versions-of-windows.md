---
description: 由於 Microsoft Windows XP 的非平板電腦版本上缺乏辨識器，因此您無法使用 InkEdit 在 windows 2000、Windows Server 2003 和非 Tablet PC 版本的 Windows XP 上轉譯筆墨，也無法使用控制項在這些作業系統上輸入筆墨。
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: 在舊版 Windows 上使用 InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971202"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a><span data-ttu-id="58c0d-103">在舊版 Windows 上使用 InkEdit</span><span class="sxs-lookup"><span data-stu-id="58c0d-103">Using InkEdit on Earlier Versions of Windows</span></span>

<span data-ttu-id="58c0d-104">由於 Microsoft Windows XP 的非平板電腦版本上缺乏辨識器，因此您無法使用 [InkEdit](inkedit-control.md) 在 windows 2000、windows Server 2003 和非 tablet pc 版本的 windows xp 上轉譯筆墨，也無法使用控制項在這些作業系統上輸入筆墨。</span><span class="sxs-lookup"><span data-stu-id="58c0d-104">Because of the lack of recognizers on non-Tablet PC editions of Microsoft Windows XP, you cannot use [InkEdit](inkedit-control.md) to render ink on Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP, and you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="58c0d-105">控制項的 [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) 屬性設定為 **停用** (針對 c + +) **\_ 停用的 IEM** ，而且嘗試變更屬性沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="58c0d-105">The control's [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property is set to **Disabled** (**IEM\_Disabled** for C++), and attempting to change the property has no effect.</span></span> <span data-ttu-id="58c0d-106">您可以將值指派給其他屬性，並將筆墨複製和貼上至其他應用程式，但您無法使用控制項來接受手勢或收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="58c0d-106">You can assign values to other properties and copy and paste ink to other applications, but you cannot use the control to accept gestures or collect ink.</span></span>

 

 



