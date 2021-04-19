---
description: 資料執行防止 (DEP) 是從 Windows XP 和 Windows Server 2003 開始的作業系統內建的系統層級記憶體保護功能。
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: 資料執行防止
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976879"
---
# <a name="data-execution-prevention"></a>資料執行防止

資料執行防止 (DEP) 是從 Windows XP 和 Windows Server 2003 開始的作業系統內建的系統層級記憶體保護功能。 DEP 可讓系統將一或多個記憶體頁面標示為無法執行檔。 將記憶體區域標記為無法執行的表示程式碼無法從該記憶體區域執行，這會使緩衝區溢位的惡意探索變得更困難。

DEP 可防止從預設堆積、堆疊和記憶體集區等資料頁面執行程式碼。 如果應用程式嘗試從受保護的資料頁執行程式碼，就會發生記憶體存取違規例外狀況，而且如果未處理例外狀況，則會結束通話進程。

DEP 並非針對所有攻擊的全面防禦，這是您可以用來保護應用程式的另一項工具。

## <a name="how-data-execution-prevention-works"></a>資料執行防護的運作方式

如果應用程式嘗試從受保護的頁面執行程式碼，則應用程式會收到狀態碼 **狀態 \_ 存取 \_ 違規** 的例外狀況。 如果您的應用程式必須從記憶體頁面執行程式碼，它必須配置並設定適當的虛擬 [記憶體保護](memory-protection.md) 屬性。 配置記憶體時，配置的記憶體必須標示為 **page \_ execute**、 **page \_ execute \_ READ**、 **page \_ execute \_ READWRITE** 或 **page \_ execute \_ WRITECOPY** 。 藉由呼叫 **malloc** 和 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 函式所進行的堆積配置是無法執行的。

應用程式無法從預設進程堆積或堆疊執行程式碼。

系統會根據開機設定資料中的「不執行頁面保護」原則設定，在系統開機時設定 DEP。 應用程式可以藉由呼叫 [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) 函數來取得目前的原則設定。 根據原則設定，應用程式可以藉由呼叫 [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) 函數來變更目前進程的 DEP 設定。

## <a name="programming-considerations"></a>程式設計考量

應用程式可以使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 函數，以適當的記憶體保護選項配置可執行檔記憶體。 建議應用程式至少設定 [ **頁面 \_ 執行** 記憶體保護] 選項。 產生可執行檔程式碼之後，建議應用程式將記憶體保護設定為不允許寫入配置的記憶體。 應用程式可以使用 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) 函式，禁止寫入配置的記憶體。 不允許寫入存取權可確保進程位址空間的可執列區域最大的保護。 您應該嘗試建立應用程式，使其使用最小的可執行位址空間，這樣可將暴露于記憶體的記憶體數量降至最低。

您也應該嘗試控制應用程式虛擬記憶體的版面配置，並建立可執行檔區域。 這些可執行檔區域應位於比無法執行區域更低的記憶體空間中。 藉由在無法執行的區域下找出可執行檔區域，您可以協助防止緩衝區溢位溢出到記憶體的可執列區域。

## <a name="application-compatibility"></a>應用程式相容性

某些應用程式功能與 DEP 不相容。 執行動態程式碼 (產生的應用程式（例如，即時產生程式碼) ，而不是使用 execute 許可權明確地標示產生的程式碼）在使用 DEP 的電腦上可能會有相容性問題。 寫入至 Active Template Library (ATL) 7.1 版及更早版本的應用程式可以嘗試在標記為無法執行的頁面上執行程式碼，這會觸發 NX 錯誤並終止應用程式;如需詳細資訊，請參閱 [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy)。 執行與 DEP 不相容之動作的大部分應用程式都必須更新，才能正常運作。

少數可執行檔和程式庫可能會在影像檔的 [資料] 區段中包含可執行程式碼。 在某些情況下，應用程式可能會將較小的程式碼區段放 (在資料區段中通常稱為 Thunk) 。 但是，除非區段已套用可執行屬性，否則 DEP 會將載入記憶體中的影像檔區段標記為無法執行的。

因此，資料區段中的可執行程式碼應該遷移至程式碼區段，或者包含可執行程式碼的資料區段應該明確標記為可執行檔。 針對包含可執行程式碼的區段，您應該將可執行檔屬性（[ **IMAGE \_ SCN \_ MEM] \_ 執行**）加入至對應區段標頭的 [ **特性** ] 欄位。 如需將屬性新增至區段的詳細資訊，請參閱連結器隨附的檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料執行防止 (TechNet) ](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[如何設定記憶體保護](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[知識庫文章875352](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
