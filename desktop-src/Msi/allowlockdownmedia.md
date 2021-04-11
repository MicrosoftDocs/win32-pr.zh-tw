---
description: 將每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034;，可讓非系統管理員的使用者從儲存在媒體上的來源（例如 cd-rom）安裝受控應用程式。
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853488"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="2aeaf-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="2aeaf-103">AllowLockdownMedia</span></span>

<span data-ttu-id="2aeaf-104">將每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可讓非系統管理員的使用者從儲存在媒體上的來源（例如 cd-rom）安裝 [*受控應用程式*](m-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="2aeaf-105">請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="2aeaf-106">例如，如果設定此原則，則非系統管理員的使用者可能會使用媒體來源來安裝已指派或已發佈的應用程式，或針對所有使用者安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="2aeaf-107">設定此原則也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="2aeaf-108">只有在執行 Windows Vista 且未加入網域的電腦上，此原則的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="2aeaf-109">在其他電腦上的預設值是，非受控使用者無法從位於媒體的來源安裝受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="2aeaf-110">因為此原則可讓非系統管理員的使用者以預設沒有的許可權安裝，所以在設定此原則之前，您應該考慮是否為使用者提供適當的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="2aeaf-111">建議使用預設設定，以確保安全的環境。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="2aeaf-112">如需保護安裝和使用數位憑證的詳細資訊，請參閱撰寫安全安裝和[數位簽章](digital-signatures-and-windows-installer.md)[的指導方針](guidelines-for-authoring-secure-installations.md)，以及 Windows Installer 以及[從網際網路下載安裝](downloading-an-installation-from-the-internet.md)。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="2aeaf-113">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="2aeaf-113">Registry Key</span></span>

<span data-ttu-id="2aeaf-114">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="2aeaf-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="2aeaf-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="2aeaf-115">Data Type</span></span>

<span data-ttu-id="2aeaf-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2aeaf-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="2aeaf-117">備註</span><span class="sxs-lookup"><span data-stu-id="2aeaf-117">Remarks</span></span>

<span data-ttu-id="2aeaf-118">如果有安裝或啟動這些程式的 Windows Installer 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。</span><span class="sxs-lookup"><span data-stu-id="2aeaf-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aeaf-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="2aeaf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aeaf-120">來源復原</span><span class="sxs-lookup"><span data-stu-id="2aeaf-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="2aeaf-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="2aeaf-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



