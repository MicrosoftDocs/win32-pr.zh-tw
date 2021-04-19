---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，安裝程式會防止非系統管理員針對安裝在電腦上的任何應用程式，使用「使用者帳戶控制」 (UAC) 修補。
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992204"
---
# <a name="disableluapatching"></a><span data-ttu-id="f79c1-103">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="f79c1-103">DisableLUAPatching</span></span>

<span data-ttu-id="f79c1-104">如果每一電腦的系統原則設定為 "1"，則安裝程式會防止非系統管理員對電腦上安裝的任何應用程式，使用「 [使用者帳戶控制」 (UAC) 修補](user-account-control--uac--patching.md) 。</span><span class="sxs-lookup"><span data-stu-id="f79c1-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="f79c1-105">當每部電腦的系統原則未設定或設定為0時，非系統管理員可以將最低許可權使用者修補程式套用至已啟用最低許可權使用者帳戶修補的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f79c1-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="f79c1-106">使用 [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) 屬性，以防止應用程式的最低許可權修補。</span><span class="sxs-lookup"><span data-stu-id="f79c1-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="f79c1-107">從 Windows Installer 版本3.0 開始，可以使用 DisableLUAPatching 原則。</span><span class="sxs-lookup"><span data-stu-id="f79c1-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="f79c1-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="f79c1-108">Registry Key</span></span>

<span data-ttu-id="f79c1-109">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f79c1-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f79c1-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="f79c1-110">Data Type</span></span>

<span data-ttu-id="f79c1-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f79c1-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="f79c1-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="f79c1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f79c1-113">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="f79c1-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



