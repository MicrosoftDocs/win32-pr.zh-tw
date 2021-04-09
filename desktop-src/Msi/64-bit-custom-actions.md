---
description: 在64位作業系統上，Windows Installer 可能會呼叫已針對32位或64位系統編譯的自訂動作。
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: 64位自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692815"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="3ddb1-103">64位自訂動作</span><span class="sxs-lookup"><span data-stu-id="3ddb1-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="3ddb1-104">在64位作業系統上，Windows Installer 可能會呼叫已針對32位或64位系統編譯的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="3ddb1-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="3ddb1-105">以 [腳本](scripts.md)為基礎的64位自訂動作必須明確標記為64位自訂動作，方法是在 [CustomAction 資料表](customaction-table.md)的類型資料行中，將 **msidbCustomActionType64BitScript** 位新增至自訂動作數數值型別。</span><span class="sxs-lookup"><span data-stu-id="3ddb1-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="3ddb1-106">常數</span><span class="sxs-lookup"><span data-stu-id="3ddb1-106">Constant</span></span>                             | <span data-ttu-id="3ddb1-107">十六進位</span><span class="sxs-lookup"><span data-stu-id="3ddb1-107">Hexadecimal</span></span> | <span data-ttu-id="3ddb1-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="3ddb1-108">Decimal</span></span> | <span data-ttu-id="3ddb1-109">意義</span><span class="sxs-lookup"><span data-stu-id="3ddb1-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="3ddb1-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="3ddb1-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="3ddb1-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="3ddb1-111">0x0001000</span></span>   | <span data-ttu-id="3ddb1-112">4096</span><span class="sxs-lookup"><span data-stu-id="3ddb1-112">4096</span></span>    | <span data-ttu-id="3ddb1-113">這是以 [腳本](scripts.md)撰寫的64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="3ddb1-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="3ddb1-114">以 [可執行檔](executable-files.md) 為基礎的自訂動作或針對64位作業系統所遵守的 [動態連結程式庫](dynamic-link-libraries.md) ，不需要在 CustomAction 資料表的 Type 資料行中包含這個額外的位。</span><span class="sxs-lookup"><span data-stu-id="3ddb1-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



