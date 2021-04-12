---
title: ADSI 和使用者帳戶控制
description: Windows 和 Windows Server 具有「使用者帳戶控制」，這對於使用 Active Directory 服務介面 (ADSI) 的應用程式有一些影響。
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024088"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="758cf-103">ADSI 和使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="758cf-103">ADSI and User Account Control</span></span>

<span data-ttu-id="758cf-104">Windows 和 Windows Server 具有「 [使用者帳戶控制](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))」，這對於使用 [Active Directory 服務介面](active-directory-service-interfaces-adsi.md) (ADSI) 的應用程式有一些影響。</span><span class="sxs-lookup"><span data-stu-id="758cf-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="758cf-105">具體來說，這些介面是設計成由具有本機電腦之系統管理員許可權的使用者帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="758cf-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="758cf-106">**問題**</span><span class="sxs-lookup"><span data-stu-id="758cf-106">**Problem**</span></span>

<span data-ttu-id="758cf-107">每次應用程式連接至目錄並嘗試建立 ADSI 物件時，都會檢查 [Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema) 是否有變更。</span><span class="sxs-lookup"><span data-stu-id="758cf-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="758cf-108">如果自上次連接以來已變更，則會下載架構並將其儲存在本機電腦上的快取中。</span><span class="sxs-lookup"><span data-stu-id="758cf-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="758cf-109">在 Windows Vista 之前的 Windows 版本中，此快取的預設位置為</span><span class="sxs-lookup"><span data-stu-id="758cf-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="758cf-110">不過，應用程式是由標準 (所執行，也就是，非系統管理員) 帳戶將無法存取此目錄，因此使用在此模式中執行的 ADSI 介面的應用程式將會在每個連接上下載架構，而這會影響輸送量和效能。</span><span class="sxs-lookup"><span data-stu-id="758cf-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="758cf-111">**方案**</span><span class="sxs-lookup"><span data-stu-id="758cf-111">**Solutions**</span></span>

<span data-ttu-id="758cf-112">*單一使用者* -若要解決此問題，有新的 ADSI 提供者登錄控制索引鍵，可決定快取 [Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema) 物件的登錄位置和檔案位置。</span><span class="sxs-lookup"><span data-stu-id="758cf-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="758cf-113">如果登錄機碼</span><span class="sxs-lookup"><span data-stu-id="758cf-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="758cf-114">設定為 0 (零) ，每位使用者將會有不同的 ADSI 儲存位置;登錄機碼將儲存在</span><span class="sxs-lookup"><span data-stu-id="758cf-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="758cf-115">和快取檔案會儲存在</span><span class="sxs-lookup"><span data-stu-id="758cf-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="758cf-116">這些設定是執行 Windows Server 2008 或 Windows Vista 之電腦上的預設設定。</span><span class="sxs-lookup"><span data-stu-id="758cf-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="758cf-117">*多使用者* -如果您在具有許多使用者帳戶的電腦上執行 ADSI 應用程式 (例如，網頁伺服器) ，則最好不要使用大量的磁碟空間來建立許多 [Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema) 快取的複本。</span><span class="sxs-lookup"><span data-stu-id="758cf-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="758cf-118">設定登錄機碼</span><span class="sxs-lookup"><span data-stu-id="758cf-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="758cf-119">至 1 (一個) 會將 ADSI 還原為先前的行為;所有 [Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema) 物件都會儲存在先前的位置;登錄機碼將會位於</span><span class="sxs-lookup"><span data-stu-id="758cf-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="758cf-120">而且快取檔案將會位於</span><span class="sxs-lookup"><span data-stu-id="758cf-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="758cf-121">在這種情況下，系統管理員帳戶應該執行應用程式，這會導致在全域位置快取架構檔案，供較少許可權的使用者日後使用。</span><span class="sxs-lookup"><span data-stu-id="758cf-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 