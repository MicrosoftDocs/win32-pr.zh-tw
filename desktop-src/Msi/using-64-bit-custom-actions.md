---
description: 在64位作業系統上，Windows Installer 可以呼叫針對32位或64位系統編譯的自訂動作。
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: 使用64位自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944643"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="b3502-103">使用64位自訂動作</span><span class="sxs-lookup"><span data-stu-id="b3502-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="b3502-104">在64位作業系統上，Windows Installer 可以呼叫針對32位或64位系統編譯的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="b3502-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="b3502-105">以 [腳本](scripts.md)為基礎的64位自訂動作必須明確標記為64位自訂動作，方法是在 [CustomAction 資料表](customaction-table.md)的類型資料行中，將 **msidbCustomActionType64BitScript** 位新增至自訂動作數數值型別。</span><span class="sxs-lookup"><span data-stu-id="b3502-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="b3502-106">以 [可執行檔](executable-files.md) 為基礎的自訂動作或針對64位作業系統所編譯的 [動態連結程式庫](dynamic-link-libraries.md) ，不需要在 CustomAction 資料表的 Type 資料行中包含這個額外的位。</span><span class="sxs-lookup"><span data-stu-id="b3502-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="b3502-107">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="b3502-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 



