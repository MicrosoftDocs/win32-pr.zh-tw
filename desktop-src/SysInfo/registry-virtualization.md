---
description: 登錄虛擬化是一種應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: 登錄虛擬化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991374"
---
# <a name="registry-virtualization"></a><span data-ttu-id="c8080-103">登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-103">Registry Virtualization</span></span>

<span data-ttu-id="c8080-104">登錄 *虛擬化* 是一種應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。</span><span class="sxs-lookup"><span data-stu-id="c8080-104">*Registry virtualization* is an application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="c8080-105">對於讀取或寫入登錄的應用程式而言，此重新導向是透明的。</span><span class="sxs-lookup"><span data-stu-id="c8080-105">This redirection is transparent to applications reading from or writing to the registry.</span></span> <span data-ttu-id="c8080-106">從 Windows Vista 開始支援。</span><span class="sxs-lookup"><span data-stu-id="c8080-106">It is supported starting with Windows Vista.</span></span>

<span data-ttu-id="c8080-107">這種形式的虛擬化是暫時的應用程式相容性技術;Microsoft 打算將它從未來版本的 Windows 作業系統中移除，因為更多應用程式都與 Windows Vista 和更新版本的 Windows 相容。</span><span class="sxs-lookup"><span data-stu-id="c8080-107">This form of virtualization is an interim application compatibility technology; Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista and later versions of Windows.</span></span> <span data-ttu-id="c8080-108">因此，您的應用程式不一定會依賴系統中的登錄虛擬化行為。</span><span class="sxs-lookup"><span data-stu-id="c8080-108">Therefore, it is important that your application does not become dependent on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="c8080-109">虛擬化的目的只是為了提供現有應用程式的相容性。</span><span class="sxs-lookup"><span data-stu-id="c8080-109">Virtualization is intended only to provide compatibility for existing applications.</span></span> <span data-ttu-id="c8080-110">針對 Windows Vista 和更新版本的 Windows 設計的應用程式不應寫入敏感性系統區域，也不應該依賴虛擬化來補救任何問題。</span><span class="sxs-lookup"><span data-stu-id="c8080-110">Applications designed for Windows Vista and later versions of Windows should not write to sensitive system areas, nor should they rely on virtualization to remedy any problems.</span></span> <span data-ttu-id="c8080-111">當更新現有的程式碼以在 Windows Vista 和更新版本的 Windows 上執行時，開發人員應該確保應用程式只會將資料儲存在每個使用者的位置，或是儲存在% alluserprofile% 內的電腦位置，以正確地使用存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="c8080-111">When updating existing code to run on Windows Vista and later versions of Windows, developers should ensure that applications only store data in per-user locations or in computer locations within %alluserprofile% that properly use an access control list (ACL).</span></span>

<span data-ttu-id="c8080-112">如需建立符合 UAC 規範之應用程式的詳細資訊，請參閱《 [Uac 開發人員指南》](/previous-versions/dotnet/articles/aa480150(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="c8080-112">For more information about building UAC-compliant applications, see the [UAC Developer Guide](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).</span></span>

## <a name="virtualization-overview"></a><span data-ttu-id="c8080-113">虛擬化總覽</span><span class="sxs-lookup"><span data-stu-id="c8080-113">Virtualization Overview</span></span>

<span data-ttu-id="c8080-114">在 Windows Vista 之前，應用程式通常是由系統管理員執行。</span><span class="sxs-lookup"><span data-stu-id="c8080-114">Prior to Windows Vista, applications were typically run by administrators.</span></span> <span data-ttu-id="c8080-115">因此，應用程式可以自由地存取系統檔案和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c8080-115">As a result, applications could freely access system files and registry keys.</span></span> <span data-ttu-id="c8080-116">如果這些應用程式是由標準使用者執行，則會因為存取權限不足而失敗。</span><span class="sxs-lookup"><span data-stu-id="c8080-116">If these applications were run by a standard user, they would fail due to insufficient access rights.</span></span> <span data-ttu-id="c8080-117">Windows Vista 和更新版本的 Windows 會自動重新導向這些作業，藉此改善應用程式的應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="c8080-117">Windows Vista and later versions of Windows improve application compatibility for these applications by automatically redirecting these operations.</span></span> <span data-ttu-id="c8080-118">例如，全域存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體** 的登錄操作，) 會重新導向至使用者設定檔中的每個使用者位置，稱為「*虛擬存放區*」 (**HKEY \_ USERS \\ <User SID> \_ 類別 \\ VirtualStore \\ 電腦 \\ 軟體**) 。</span><span class="sxs-lookup"><span data-stu-id="c8080-118">For example, registry operations to the global store (**HKEY\_LOCAL\_MACHINE\\Software**) are redirected to a per-user location within the user's profile known as the *virtual store* (**HKEY\_USERS\\<User SID>\_Classes\\VirtualStore\\Machine\\Software**).</span></span>

<span data-ttu-id="c8080-119">登錄虛擬化可以廣泛分類為下列類型：</span><span class="sxs-lookup"><span data-stu-id="c8080-119">Registry virtualization can be broadly classified into the following types:</span></span>

<dl> <dt>

<span data-ttu-id="c8080-120"><span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>開啟登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-120"><span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Open Registry Virtualization</span></span>
</dt> <dd>

<span data-ttu-id="c8080-121">如果呼叫端沒有金鑰的寫入權限，而且嘗試開啟金鑰，則會以該呼叫者的最大允許存取來開啟金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8080-121">If the caller does not have write access to a key and attempts to open the key, the key is opened with the maximum allowed access for that caller.</span></span>

<span data-ttu-id="c8080-122">如果登錄機 \_ 碼 \_ 不 \_ \_ 會針對機碼設定無訊息失敗旗標，則作業會失敗，且不會開啟金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8080-122">If the REG\_KEY\_DONT\_SILENT\_FAIL flag is set for the key, the operation fails and the key is not opened.</span></span> <span data-ttu-id="c8080-123">如需詳細資訊，請參閱本主題稍後的「控制登錄虛擬化」。</span><span class="sxs-lookup"><span data-stu-id="c8080-123">For more information, see "Controlling Registry Virtualization" later in this topic.</span></span>

</dd> <dt>

<span data-ttu-id="c8080-124"><span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>撰寫登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-124"><span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Write Registry Virtualization</span></span>
</dt> <dd>

<span data-ttu-id="c8080-125">如果呼叫端沒有金鑰的寫入存取權，並嘗試將值寫入其中或建立子機碼，則會將值寫入虛擬存放區。</span><span class="sxs-lookup"><span data-stu-id="c8080-125">If the caller does not have write access to a key and attempts to write a value to it or create a subkey, the value is written to the virtual store.</span></span>

<span data-ttu-id="c8080-126">例如，如果受限的使用者嘗試將值寫入下列機碼： **HKEY \_ 本機 \_ 電腦 \\ 軟體** \\ *AppKey1*，虛擬化會將寫入作業重新導向至 **HKEY \_ 使用者 \\ <User SID> \_ 類別 \\ VirtualStore \\ 電腦 \\ 軟體** \\ *AppKey1*。</span><span class="sxs-lookup"><span data-stu-id="c8080-126">For example, if a limited user attempts to write a value to the following key: **HKEY\_LOCAL\_MACHINE\\Software**\\*AppKey1*, virtualization redirects the write operation to **HKEY\_USERS\\<User SID>\_Classes\\VirtualStore\\Machine\\Software**\\*AppKey1*.</span></span>

</dd> <dt>

<span data-ttu-id="c8080-127"><span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>讀取登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-127"><span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Read Registry Virtualization</span></span>
</dt> <dd>

<span data-ttu-id="c8080-128">如果呼叫端從已虛擬化的機碼讀取，則登錄會顯示虛擬化值 (從虛擬存放區) 和 (從全域存放區) 到呼叫端的非虛擬值的合併觀點。</span><span class="sxs-lookup"><span data-stu-id="c8080-128">If the caller reads from a key that is virtualized, the registry presents a merged view of both the virtualized values (from the virtual store) and the non-virtual values (from the global store) to the caller.</span></span>

<span data-ttu-id="c8080-129">例如，假設 **HKEY \_ LOCAL \_ MACHINE \\ Software** \\ *AppKey1* 包含兩個值 V1 和 V2，而且限制使用者將值 V3 寫入機碼。</span><span class="sxs-lookup"><span data-stu-id="c8080-129">For example, suppose **HKEY\_LOCAL\_MACHINE\\Software**\\*AppKey1* contains two values V1 and V2 and that a limited user writes a value V3 to the key.</span></span> <span data-ttu-id="c8080-130">當使用者嘗試從此索引鍵讀取值時，合併的視圖會包含來自全域存放區的值 V1 和 V2，以及來自虛擬存放區的值 V3。</span><span class="sxs-lookup"><span data-stu-id="c8080-130">When the user attempts to read values from this key, the merged view includes values V1 and V2 from the global store and value V3 from the virtual store.</span></span>

<span data-ttu-id="c8080-131">請注意，虛擬值會優先于全域值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c8080-131">Note that virtual values take precedence over global values when present.</span></span> <span data-ttu-id="c8080-132">在上述範例中，即使全域存儲區在此機碼底下具有值 V3，值 V3 仍會從虛擬存放區傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="c8080-132">In the example above, even if the global store had value V3 under this key, the value V3 would still be returned to the caller from the virtual store.</span></span> <span data-ttu-id="c8080-133">如果要從虛擬存放區刪除 V3，則會從全域存放區傳回 V3。</span><span class="sxs-lookup"><span data-stu-id="c8080-133">If V3 were to be deleted from the virtual store, then V3 would be returned from the global store.</span></span> <span data-ttu-id="c8080-134">換句話說，如果 V3 要從 **HKEY \_ USERS 類別中刪除 \\ <User SID> \_ \\ VirtualStore \\ Machine \\ software** \\ *AppKey1* 但是 **HKEY \_ LOCAL \_ Machine \\ software** \\ *AppKey1* 具有值 V3，則會從全域存放區傳回該值。</span><span class="sxs-lookup"><span data-stu-id="c8080-134">In other words, if V3 were to be deleted from **HKEY\_USERS\\<User SID>\_Classes\\VirtualStore\\Machine\\Software**\\*AppKey1* but **HKEY\_LOCAL\_MACHINE\\Software**\\*AppKey1* had a value V3, then that value would be returned from the global store.</span></span>

</dd> </dl>

## <a name="registry-virtualization-scope"></a><span data-ttu-id="c8080-135">登錄虛擬化範圍</span><span class="sxs-lookup"><span data-stu-id="c8080-135">Registry Virtualization Scope</span></span>

<span data-ttu-id="c8080-136">登錄虛擬化只會針對下列各項啟用：</span><span class="sxs-lookup"><span data-stu-id="c8080-136">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="c8080-137">32位的互動式進程。</span><span class="sxs-lookup"><span data-stu-id="c8080-137">32-bit interactive processes.</span></span>
-   <span data-ttu-id="c8080-138">**HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8080-138">Keys in **HKEY\_LOCAL\_MACHINE\\Software**.</span></span>
-   <span data-ttu-id="c8080-139">系統管理員可以寫入的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8080-139">Keys that an administrator can write to.</span></span> <span data-ttu-id="c8080-140"> (如果系統管理員無法寫入金鑰，則應用程式在舊版的 Windows 上會失敗，即使是由系統管理員執行也一樣。 ) </span><span class="sxs-lookup"><span data-stu-id="c8080-140">(If an administrator cannot write to a key, then the application would have failed on previous versions of Windows even if it was run by an administrator.)</span></span>

<span data-ttu-id="c8080-141">已針對下列各項停用登錄虛擬化：</span><span class="sxs-lookup"><span data-stu-id="c8080-141">Registry virtualization is disabled for the following:</span></span>

-   <span data-ttu-id="c8080-142">64位進程。</span><span class="sxs-lookup"><span data-stu-id="c8080-142">64-bit processes.</span></span>
-   <span data-ttu-id="c8080-143">不是互動式的進程，例如服務。</span><span class="sxs-lookup"><span data-stu-id="c8080-143">Processes that are not interactive, such as services.</span></span>

    <span data-ttu-id="c8080-144">請注意，使用登錄作為處理序間通訊 () 服務 (或未) 啟用虛擬化之任何其他進程之間的 IPC 機制，而且如果金鑰已虛擬化，應用程式將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c8080-144">Note that using the registry as an inter-process communication (IPC) mechanism between a service (or any other process that does not have virtualization enabled) and an application will not work correctly if the key is virtualized.</span></span> <span data-ttu-id="c8080-145">比方說，如果防毒軟體服務根據應用程式所設定的值來更新其簽章檔案，服務將永遠不會更新其簽章檔案，因為服務會讀取全域存放區，但應用程式會寫入虛擬存放區。</span><span class="sxs-lookup"><span data-stu-id="c8080-145">For instance, if an antivirus service updates its signature files based on a value set by an application, the service will never update its signature files because the service reads from the global store but the application writes to the virtual store.</span></span>

-   <span data-ttu-id="c8080-146">模擬使用者的進程。</span><span class="sxs-lookup"><span data-stu-id="c8080-146">Processes that impersonate a user.</span></span> <span data-ttu-id="c8080-147">如果進程在模擬使用者時嘗試操作，該作業將不會虛擬化。</span><span class="sxs-lookup"><span data-stu-id="c8080-147">If a process attempts an operation while impersonating a user, that operation will not be virtualized.</span></span>
-   <span data-ttu-id="c8080-148">核心模式進程，例如驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c8080-148">Kernel-mode processes such as drivers.</span></span>
-   <span data-ttu-id="c8080-149">在資訊清單中指定 **並無 requestedexecutionlevel** 的進程。</span><span class="sxs-lookup"><span data-stu-id="c8080-149">Processes that have **requestedExecutionLevel** specified in their manifests.</span></span>
-   <span data-ttu-id="c8080-150">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 的金鑰和子機碼、 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ Windows**，以及 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ Windows NT**。</span><span class="sxs-lookup"><span data-stu-id="c8080-150">Keys and subkeys of **HKEY\_LOCAL\_MACHINE\\Software\\Classes**, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows**, and **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT**.</span></span>

## <a name="controlling-registry-virtualization"></a><span data-ttu-id="c8080-151">控制登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-151">Controlling Registry Virtualization</span></span>

<span data-ttu-id="c8080-152">除了在資訊清單中使用 **並無 requestedexecutionlevel** 來控制應用層級的虛擬化，系統管理員還可以針對 **HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰，以每個金鑰為基礎來啟用或停用虛擬化。</span><span class="sxs-lookup"><span data-stu-id="c8080-152">In addition to controlling virtualization at an application level by using **requestedExecutionLevel** in the manifest, an administrator can enable or disable virtualization on a per-key basis for keys in **HKEY\_LOCAL\_MACHINE\\Software**.</span></span> <span data-ttu-id="c8080-153">若要這樣做，請使用 Reg.exe 命令列公用程式旗標選項以及下表所列的旗標。</span><span class="sxs-lookup"><span data-stu-id="c8080-153">To do this, use the Reg.exe command-line utility FLAGS option with the flags listed in the following table.</span></span>



| <span data-ttu-id="c8080-154">旗標</span><span class="sxs-lookup"><span data-stu-id="c8080-154">Flag</span></span>                         | <span data-ttu-id="c8080-155">意義</span><span class="sxs-lookup"><span data-stu-id="c8080-155">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8080-156">REG 機碼不是無訊息的 \_ \_ \_ \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="c8080-156">REG\_KEY\_DONT\_SILENT\_FAIL</span></span> | <span data-ttu-id="c8080-157">此旗標會停用開啟的登錄虛擬化。</span><span class="sxs-lookup"><span data-stu-id="c8080-157">This flag disables open registry virtualization.</span></span> <span data-ttu-id="c8080-158">如果設定此旗標，且已啟用虛擬化的金鑰上的開啟作業失敗，則登錄不會嘗試重新開啟金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8080-158">If this flag is set and an open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="c8080-159">如果清除此旗標，登錄會嘗試以允許的最大存取權來重新開啟金鑰， \_ 而不是所要求的存取權。</span><span class="sxs-lookup"><span data-stu-id="c8080-159">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access instead of the requested access.</span></span>                                                                   |
| <span data-ttu-id="c8080-160">REG 機碼不會 \_ \_ \_ 虛擬化</span><span class="sxs-lookup"><span data-stu-id="c8080-160">REG\_KEY\_DONT\_VIRTUALIZE</span></span>   | <span data-ttu-id="c8080-161">此旗標會停用寫入登錄虛擬化。</span><span class="sxs-lookup"><span data-stu-id="c8080-161">This flag disables write registry virtualization.</span></span> <span data-ttu-id="c8080-162">如果設定此旗標，且 create key 或 set value 作業失敗，因為呼叫端沒有父機碼的足夠存取權限，則登錄會導致作業失敗。</span><span class="sxs-lookup"><span data-stu-id="c8080-162">If this flag is set and a create key or set value operation fails because the caller does not have sufficient access right to the parent key, the registry fails the operation.</span></span> <span data-ttu-id="c8080-163">如果清除此旗標，登錄會嘗試寫入虛擬存放區中的機碼或值。</span><span class="sxs-lookup"><span data-stu-id="c8080-163">If this flag is clear, the registry attempts to write the key or value in the virtual store.</span></span> <span data-ttu-id="c8080-164">呼叫 \_ 端必須在父機碼上具有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="c8080-164">The caller must have the KEY\_READ right on the parent key.</span></span> |
| <span data-ttu-id="c8080-165">REG \_ KEY \_ 遞迴 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="c8080-165">REG\_KEY\_RECURSE\_FLAG</span></span>      | <span data-ttu-id="c8080-166">如果設定此旗標，則會從父機碼傳播登錄虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="c8080-166">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="c8080-167">如果清除此旗標，則不會傳播登錄虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="c8080-167">If this flag is clear, registry virtualization flags are not propagated.</span></span> <span data-ttu-id="c8080-168">變更此旗標只會影響在旗標變更之後所建立的新子索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c8080-168">Changing this flag affects only new descendent keys created after the flag is changed.</span></span> <span data-ttu-id="c8080-169">它不會針對現有的子機碼設定或清除這些旗標。</span><span class="sxs-lookup"><span data-stu-id="c8080-169">It does not set or clear these flags for existing descendent keys.</span></span>                                                                  |



 

<span data-ttu-id="c8080-170">下列範例示範如何使用 Reg.exe 命令列公用程式搭配 FLAGS 選項，以查詢金鑰之虛擬化旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8080-170">The following example shows the use of the Reg.exe command-line utility with the FLAGS option to query the state of the virtualization flags for a key.</span></span>

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

<span data-ttu-id="c8080-171">每次在虛擬機器上啟用審核功能時，系統就會產生新的虛擬化 audit 事件，以指出金鑰已虛擬化 (一般的 audit 事件) 。</span><span class="sxs-lookup"><span data-stu-id="c8080-171">Whenever auditing is enabled on a key that is being virtualized, a new virtualization audit event is generated to indicate that the key is being virtualized (addition to the usual audit events).</span></span> <span data-ttu-id="c8080-172">系統管理員可以使用這項資訊來監視系統上虛擬化的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8080-172">Administrators can use this information to monitor the status of virtualization on their systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8080-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8080-173">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8080-174">[使用使用者帳戶控制開始使用](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="c8080-174">[Getting Started with User Account Control](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="c8080-175">[瞭解及設定使用者帳戶控制](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c8080-175">[Understanding and Configuring User Account Control](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="c8080-176">[最低許可權環境中應用程式的開發人員最佳做法和指導方針](/previous-versions/dotnet/articles/aa480150(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c8080-176">[Developer Best Practices and Guidelines for Applications in a Least Privileged Environment](/previous-versions/dotnet/articles/aa480150(v=msdn.10))</span></span>
</dt> </dl>

 

 
