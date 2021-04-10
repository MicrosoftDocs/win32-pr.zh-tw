---
description: 如果此每部電腦系統原則的值設定為 &\# 0034; 2&\# 0034; 所有應用程式的安裝程式一律為停用。 如果此原則值設定為 &\# 0034; 1&\# 0034;，則會停用未受管理應用程式的安裝程式，但仍會針對受控應用程式啟用。
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026883"
---
# <a name="disablemsi"></a><span data-ttu-id="d0fcb-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="d0fcb-104">DisableMSI</span></span>

<span data-ttu-id="d0fcb-105">如果每部電腦 [系統原則](system-policy.md) 的值設定為 "2"，則所有應用程式一律會停用安裝程式。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="d0fcb-106">如果此原則值設定為 "1"，則會停用未受管理應用程式的安裝程式，但仍會針對受控應用程式啟用。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="d0fcb-107">下表列出可能的設定。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="d0fcb-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="d0fcb-108">DisableMSI</span></span> | <span data-ttu-id="d0fcb-109">描述</span><span class="sxs-lookup"><span data-stu-id="d0fcb-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fcb-110">*預設值*</span><span class="sxs-lookup"><span data-stu-id="d0fcb-110">*Default*</span></span>  | <span data-ttu-id="d0fcb-111">在 Windows Server 2003、Windows Server 2003 R2、Windows Server 2008 和 Windows Server 2008 R2 上，如果原則值為 Null、不存在，或1或2以外的任何數位，則會為受控應用程式啟用 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="d0fcb-112">系統會封鎖非受控應用程式安裝。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="d0fcb-113">在 Windows XP、Windows Vista 和 Windows 7 上，會針對所有應用程式啟用 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="d0fcb-114">允許所有安裝作業。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="d0fcb-115">0</span><span class="sxs-lookup"><span data-stu-id="d0fcb-115">0</span></span>          | <span data-ttu-id="d0fcb-116">所有應用程式都已啟用 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="d0fcb-117">允許所有安裝作業。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d0fcb-118">1</span><span class="sxs-lookup"><span data-stu-id="d0fcb-118">1</span></span>          | <span data-ttu-id="d0fcb-119">未受管理的應用程式會停用 Windows Installer，但仍會為受控應用程式啟用。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="d0fcb-120">系統會封鎖非提高許可權的每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="d0fcb-121">允許每位使用者的提高許可權，以及每部電腦的安裝。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="d0fcb-122">2</span><span class="sxs-lookup"><span data-stu-id="d0fcb-122">2</span></span>          | <span data-ttu-id="d0fcb-123">所有應用程式一律會停用 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="d0fcb-124">不允許安裝，包括修復、重新安裝或隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="d0fcb-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="d0fcb-125">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="d0fcb-125">Registry Key</span></span>

<span data-ttu-id="d0fcb-126">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d0fcb-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d0fcb-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="d0fcb-127">Data Type</span></span>

<span data-ttu-id="d0fcb-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d0fcb-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0fcb-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0fcb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0fcb-130">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="d0fcb-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




