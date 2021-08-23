---
description: SelfRegModules 動作會處理 SelfReg 資料表中所列的所有模組，並向系統註冊所有已安裝的模組。 安裝程式不會自行註冊 EXE 檔案。
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: SelfRegModules 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf137dc63baa72a3d5b93370e40911af93691eaa911c4081990656c84091870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630038"
---
# <a name="selfregmodules-action"></a>SelfRegModules 動作

SelfRegModules 動作會處理 [SelfReg](selfreg-table.md) 資料表中所列的所有模組，並向系統註冊所有已安裝的模組。 安裝程式不會自行註冊 EXE 檔案。

## <a name="sequence-restrictions"></a>順序限制

呼叫 SelfRegModules 動作之前，必須先呼叫 [InstallValidate](installvalidate-action.md) 動作。 如果使用 [InstallFiles](installfiles-action.md) 動作，它必須出現在序列中的 SelfRegModules 動作之前。 因為 SelfRegModules 動作會變更系統，所以 SelfRegModules 應該在 [InstallInitialize 動作](installinitialize-action.md)之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                           |
|-------|------------------------------------------------------|
| \[1\] | 已註冊模組檔案的識別碼。                |
| \[2\] | 保存已註冊模組檔案的資料夾識別碼。 |



 

## <a name="remarks"></a>備註

SelfRegModules 動作會嘗試呼叫已排程要註冊之模組的 [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 函式。 當以較高的許可權執行安裝時，此動作會以較高的許可權執行，例如在個別電腦安裝期間。 在每一使用者安裝期間，安裝程式會以使用者權限執行此動作。

請注意，您無法使用 [SelfUnRegModules 動作](selfunregmodules-action.md)來指定安裝程式註冊自我註冊 dll 的順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定自我註冊的順序](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
