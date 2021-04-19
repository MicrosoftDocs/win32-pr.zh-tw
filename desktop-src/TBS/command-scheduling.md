---
title: 命令排程
description: 每個命令都有與其相關聯的優先順序。
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967626"
---
# <a name="command-scheduling"></a>命令排程

## <a name="command-scheduling"></a>命令排程

您可以隨時從多個內容將命令提交至 TB。 不過，實體 TPM 一次只能處理一個命令，而某些命令可能會執行一段很長的時間。 當有多個命令暫止時，TBS 會決定要傳送至 TPM 的命令。 提交命令時，每個命令都會有相關聯的優先順序。 TBS 會使用這些優先順序來判斷每次 TPM 免費時要提交的暫止命令。 這四個優先權等級為 low、normal、high 和 system。 應用程式應該使用低、一般或高優先順序。 雖然高優先順序的命令通常會在低優先順序的命令之前執行，但 [TB] 命令排程器具有過時原則，最終會為已封鎖的命令提供非常高的優先權。

## <a name="context-management"></a>內容管理

\_使用虛擬控制碼將 TPM SaveCoNtext 或 TPM2 CoNtextSave 命令提交到 TBS 所管理的資源時，會在實體資源上執行適當的命令，並將結果傳回給呼叫者（如果資源實際上存在於 TPM 中）。 如果資源實際上不在 TPM 中，則 TPM \_ SaveCoNtext 或 TPM2 CoNtextSave 命令的前置處理 \_ 會導致重新載入資源，此時內容將會儲存並傳回給呼叫端。 如果儲存的資源類型通常會在儲存後自動從 TPM 自動排清，則在完成此命令時，會使虛擬資源失效。 將 TPM \_ LoadCoNtext 或 TPM2 \_ CoNtextLoad 命令提交到 tb 時，tb 會立即執行命令。 如果命令成功完成，則會將資源控制碼虛擬化，並將產生的 TPM 位元組串流傳遞給呼叫端。 \_使用虛擬控制碼將 tpm FlushSpecific 或 TPM2 \_ FlushCoNtext 命令提交到 TBS 所管理的資源時，此 tb 會執行 tpm \_ FlushSpecific 或 TPM2 \_ FlushCoNtext 命令，以從 tpm 中收回資源（如果實際上有的話）。 在此情況下，TBS 會使虛擬資源失效，並將 flush 命令的結果傳回給呼叫者。 如果資源實際上不存在於 TPM 中，則 TPM \_ FlushSpecific 或 TPM2 \_ FlushCoNtext 命令的前置處理會載入對應于虛擬控制碼的資源，但它會在實際處理命令時進行清除。 此 TB 不支援 tpm \_ KeyControlOwner 位或 tpm LoadCoNtext 作業的 keepHandle 功能 \_ ，因此它不會為資源提供儲存內容之前的相同處理常式。

## <a name="other-commands"></a>其他命令

本檔中未提及的命令會藉由在) 必要時將虛擬金鑰控制碼取代 (的實體金鑰控制碼來處理，並將其提交至 TPM。 這是在執行適當的作業之後完成，以確保所使用的資源實際上存在於 TPM 上。 不會執行其他特殊處理。 只要修改從 TPM 傳回的資料做為 TPM \_ GetCapabilities 或 TPM2 GetCapability 查詢的一部分，此 tb 就不會嘗試改善虛擬化的精確度 \_ 。 此 TB 也支援 TCG 實體存在性命令。 此 TB 可作為實體存在性命令的傳遞：TBS 本身不會執行任何特殊處理。

## <a name="cleanup"></a>清除

當內容結束時，與其相關聯的所有實體和虛擬資源都會清除，使其不再耗用系統資源。

 

 




