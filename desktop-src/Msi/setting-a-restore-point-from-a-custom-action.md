---
description: 自訂動作不得呼叫 SRSetRestorePoint 函式，因為這可能會導致將還原進入點寫入 Windows Installer 安裝的中間。
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: 設定自訂動作的還原點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115825"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a><span data-ttu-id="cf09d-103">設定自訂動作的還原點</span><span class="sxs-lookup"><span data-stu-id="cf09d-103">Setting a Restore Point from a Custom Action</span></span>

<span data-ttu-id="cf09d-104">自訂動作不得呼叫 [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) 函式，因為這可能會導致將還原進入點寫入 Windows Installer 安裝的中間。</span><span class="sxs-lookup"><span data-stu-id="cf09d-104">Custom actions must not call the [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) function because this may result in a restore entry point being written into the middle of a Windows Installer installation.</span></span>

<span data-ttu-id="cf09d-105">如需詳細資訊，請參閱 [系統還原點和 Windows Installer](system-restore-points-and-the-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="cf09d-105">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md).</span></span>

 

 
