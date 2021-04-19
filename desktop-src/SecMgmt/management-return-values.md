---
description: 列出安全性管理函數所傳回的值。
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: 安全性管理傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997896"
---
# <a name="security-management-return-values"></a>安全性管理傳回值

安全性管理傳回值包括下列各項：

-   [附件傳回值](#attachment-return-values)
-   [LSA 原則函數傳回值](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>附件傳回值

安全性設定工具組支援下列 **SCESTATUS** 傳回碼。 這些值是由附件支援函式所傳回，以及在撰寫附件引擎或嵌入式管理單元時所實行的函式。



| 值                            | 描述                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ 成功               | 此函數已成功。                                                                          |
| SCESTATUS \_ 不正確 \_ 參數    | 傳遞給函數的其中一個參數無效。                                      |
| \_ \_ 找不到 SCESTATUS 記錄 \_    | 在安全性資料庫中找不到指定的記錄。                                     |
| SCESTATUS \_ 不正確 \_ 資料         | 因為某些資料無效，所以函數失敗。                                             |
| SCESTATUS \_ 物件 \_ 存在        | 物件已存在。                                                                       |
| SCESTATUS \_ 緩衝區 \_ 太 \_ 小    | 傳入函數以接收資料的緩衝區不夠大，無法接收所有資料。 |
| \_ \_ 找不到 SCESTATUS 設定檔 \_   | 找不到指定的設定檔。                                                             |
| SCESTATUS \_ 錯誤 \_ 格式           | 格式無效。                                                                         |
| SCESTATUS 不足的 \_ \_ \_ 資源 | 記憶體不足。                                                                    |
| \_拒絕 SCESTATUS 存取 \_        | 呼叫端沒有足夠的許可權來完成此動作。                          |
| SCESTATUS \_ 無法 \_ 刪除          | 函數無法刪除指定的專案。                                                   |
| SCESTATUS \_ 前置詞 \_ 溢位      | 發生前置詞溢位。                                                                      |
| SCESTATUS \_ 其他 \_ 錯誤          | 發生未指定的錯誤。                                                               |
| SCESTATUS \_ 已在執行 \_      | 服務已在執行中。                                                                  |
| SCESTATUS \_ 服務 \_ 不 \_ 支援 | 不支援指定的服務。                                                          |
| \_ \_ 找不到 SCESTATUS MOD \_       | 找不到或無法載入登錄中所列的附件引擎 DLL。      |
| \_ \_ 伺服器中的 SCESTATUS 例外狀況 \_ | 伺服器發生例外狀況。                                                             |



 

## <a name="lsa-policy-function-return-values"></a>LSA 原則函數傳回值

大部分的 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 原則函式會傳回可表示成功或失敗的 NTSTATUS 值。 各種的 NTSTATUS 值都是在與 Microsoft Windows 驅動程式開發工具組一起散發 (DDK) 的 Ntstatus 中定義。

若要將 NTSTATUS 傳回值轉換成 Windows 錯誤碼，請使用 [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) 函數。

下表列出任何 LSA 函數可能傳回的 NTSTATUS 值。  (部分 LSA 函式的傳回值區段會列出函式可能會傳回的其他錯誤碼。 ) 此資料表也會列出對應至每個每個 NTSTATUS 值的 Windows 錯誤碼。



|  (Windows 錯誤碼的 NTSTATUS 程式碼)                                         | 意義                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 狀態 \_ 成功 (錯誤 \_ 成功) <br/>                               | 函數成功。                                                                                                            |
| 拒絕狀態 \_ 存取 \_ (\_ 拒絕存取錯誤 \_) <br/>                 | 呼叫端沒有適當的存取權，無法完成此作業。                                                                  |
| 狀態 \_ \_ 資源不足 (錯誤 \_) 沒有任何 \_ 系統 \_ 資源<br/> | 沒有足夠的系統資源 (例如記憶體來配置緩衝區) 來完成呼叫。                                        |
| 狀態 \_ 內部 \_ 資料庫 \_ 錯誤 (錯誤 \_ 內部 \_ 資料庫 \_ 錯誤) <br/>       | LSA 資料庫包含內部不一致的情況。                                                                                    |
| 狀態 \_ 不正確 \_ 控制碼 (錯誤 \_ 不正確 \_ 控制碼) <br/>               | 表示在使用的 [*內容*](/windows/desktop/SecGloss/c-gly) 中，物件或 RPC 控制碼無效。     |
| 狀態 \_ 不正確 \_ 伺服器 \_ 狀態 (錯誤 \_ 不正確 \_ 伺服器 \_ 狀態) <br/> | 指出 LSA 伺服器目前已停用。                                                                                         |
| 狀態 \_ 不正確 \_ 參數 (錯誤 \_ 不正確 \_ 參數) <br/>         | 其中一個參數無效。                                                                                                     |
| 狀態沒有這類許可權 \_ \_ \_ (\_ 錯誤 \_ \_) <br/>       | 指出指定的許可權不存在。                                                                                         |
| 找不到狀態 \_ 物件 \_ 名稱 \_ \_ (\_ \_ 找不 \_ 到錯誤檔案) <br/>     | 在 LSA 原則資料庫中找不到物件。 物件可能已依 SID 或名稱指定，視其類型而定。 |
| 狀態不 \_ 成功 (錯誤 \_ GEN \_ 失敗) <br/>                     | 一般失敗，例如 RPC 連接失敗。                                                                                        |



 

 

