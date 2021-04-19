---
description: 您可以使用 InkPicture 控制項，在 Microsoft Windows 2000、Windows Server 2003 和非 Tablet PC 版本的 Windows XP 上呈現筆墨。 不過，您無法使用控制項在這些作業系統上輸入筆墨。
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: 在舊版 Windows 上使用 InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973255"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="ef509-104">在舊版 Windows 上使用 InkPicture</span><span class="sxs-lookup"><span data-stu-id="ef509-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="ef509-105">您可以使用 [InkPicture 控制項](inkpicture-control.md) ，在 Microsoft windows 2000、windows Server 2003 和非 Tablet PC 版本的 windows XP 上呈現筆墨。</span><span class="sxs-lookup"><span data-stu-id="ef509-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="ef509-106">不過，您無法使用控制項在這些作業系統上輸入筆墨。</span><span class="sxs-lookup"><span data-stu-id="ef509-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="ef509-107">控制項的 [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) 屬性設定為 **FALSE**，而且嘗試變更屬性沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="ef509-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="ef509-108">您可以將值指派給其他屬性，並以程式設計方式操作筆墨，但是您無法使用控制項來收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="ef509-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



