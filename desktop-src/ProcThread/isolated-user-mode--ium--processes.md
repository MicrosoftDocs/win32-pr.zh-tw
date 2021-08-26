---
description: Windows 10 引進了新的安全性功能，名為虛擬安全模式 (VSM) 。
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: 隔離的使用者模式 (IUM) 進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982d9924f60d02a74aa7237e5c3bb16e787f1d3a0cc07e9693e9cd47335cedc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032533"
---
# <a name="isolated-user-mode-ium-processes"></a>隔離的使用者模式 (IUM) 進程

Windows 10 引進了新的安全性功能，名為虛擬安全模式 (VSM) 。 VSM 利用 Hyper-v 管理程式和第二層位址轉譯 (SLAT) 來建立一組稱為虛擬信任層級的模式 (Vtl) 。 這個新的軟體架構會建立安全性界限，以防止在某個 VTL 中執行的進程存取另一個 VTL 的記憶體。 這項隔離的好處包括：減少核心攻擊的額外風險，同時保護密碼雜湊和 Kerberos 金鑰之類的資產。

圖1說明傳統的核心模式和使用者模式程式碼（分別在 CPU ring 0 和 ring 3 中執行）的模型。 在此新模型中，傳統模型中執行的程式碼會在 VTL0 中執行，而且它無法存取較高許可權的 VTL1，其中安全核心和隔離使用者模式 (IUM) 執行程式碼。 Vtl 是階層表示在 VTL1 中執行的任何程式碼，比在 VTL0 中執行的程式碼更有許可權。

VTL 隔離是由 Hyper-v 虛擬程式所建立，它會在開機時使用第二層位址轉譯 (SLAT) 來指派記憶體。 當系統執行時，它會以動態方式繼續進行，保護安全核心所指定的記憶體需要防止 VTL0，因為它會用來包含秘密。 針對這兩個 Vtl 配置個別的記憶體區塊時，系統會為 VTL1 建立安全的執行時間環境，方法是將專屬的記憶體區塊指派給 VTL1，並使用適當的存取權限來 VTL0。

**圖 1-IUM 架構**

![圖 1-ium 架構](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (也稱為受信任的進程、安全程式或 IUM 程式，) 是在 VSM 中以 IUM 進程的形式執行的程式。 他們藉由將系統呼叫封送處理至 VTL0 環形0中執行的 Windows 核心來完成系統呼叫。 VSM 建立了一個小型的執行環境，其中包含在 VTL1 中執行的小型安全核心， (與 VTL0) 中執行的核心和驅動程式隔離。 明確的安全性優點是從 VTL0 核心中執行的驅動程式，將 VTL1 中的 trustlet 使用者模式頁面隔離。 即使 VTL0 的核心模式遭到惡意程式碼入侵，它也無法存取 IUM 進程頁面。

啟用 VSM 之後， (LSASS) 環境的本地安全機構會以 trustlet 的形式執行。 LSASS 會管理本機系統原則、使用者驗證，以及處理機密安全性資料（例如密碼雜湊和 Kerberos 金鑰）的審核。 為了充分利用 VSM 的安全性優勢，名為)  (LSAISO.exe 的 trustlet 會在 VTL1 中執行，並透過 RPC 通道與 VTL0 中執行的 LSASS.exe 進行通訊。 LSAISO 秘密會先經過加密，再將它們傳送到以 VSM 正常模式執行的 LSASS，而且 LSAISO 的頁面會受到保護，以防止惡意程式碼在 VTL0 中執行。

**圖2– LSASS Trustlet 設計**

![圖2– lsass trustlet 設計 ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>隔離的使用者模式 (IUM) 含意

您無法附加到 IUM 進程，而是抑制偵錯工具 VTL1 程式碼的能力。 這包括事後剖析記憶體傾印的偵錯工具，以及附加偵錯工具來進行即時的偵錯工具。 它也包含特殊許可權帳戶或核心驅動程式的嘗試，以將 DLL 載入至 IUM 程式、插入執行緒或傳遞使用者模式。 這類嘗試可能會導致整個系統不穩定。 Windows危及 Trustlet 安全性的 Api 可能會以非預期的方式失敗。 例如，將 DLL 載入至 Trustlet 可在 VTL0 中使用，但不能在 VTL1 中使用。 如果目標執行緒在 Trustlet 中，QueueUserApc 可能會無訊息地失敗。 當針對 Trustlets 使用時，其他 Api （例如 CreateRemoteThread、VirtualAllocEx 和 Read/WriteProcessMemory）也將無法如預期般運作。

使用下面的範例程式碼，以防止呼叫任何嘗試將程式碼附加或插入至 IUM 進程的函式。 這包括將 Apc 排入佇列以在 trustlet 中執行程式碼的核心驅動程式。

## <a name="remarks"></a>備註

如果 IsSecureProcess 的傳回狀態為 success，請檢查 SecureProcess \_ Out \_ 參數，以判斷進程是否為 IUM 進程。 系統會將 IUM 處理常式標示為「安全進程」。 TRUE 的布林值結果表示目標進程的類型為 IUM。


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



Windows 10 "Windows 驅動程式套件-Windows 10. 0.15063.0" 的 WDK 包含處理常式 \_ 延伸 \_ 基本資訊結構的必要定義 \_ 。 結構的更新版本是在 ntddk 中以新的 IsSecureProcess 欄位定義。


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



