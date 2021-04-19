---
description: SelfUnregModules 動作會將 SelfReg 資料表中所列的所有模組取消註冊，而這些模組已排程要卸載。 安裝程式不會自行註冊。EXE 檔案。
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: SelfUnregModules 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996997"
---
# <a name="selfunregmodules-action"></a>SelfUnregModules 動作

SelfUnregModules 動作會將 [SelfReg 資料表](selfreg-table.md) 中所列的所有模組取消註冊，而這些模組已排程要卸載。 安裝程式不會自行註冊。EXE 檔案。

## <a name="sequence-restrictions"></a>順序限制

[InstallValidate](installvalidate-action.md)動作必須出現在序列中的 SelfUnregModules 動作之前。 如果使用 [SelfRegModules](selfregmodules-action.md) 動作，它必須出現在序列中的 SelfUnregModules 動作之後。 如果使用 [RemoveFiles 動作](removefiles-action.md) ，它必須出現在序列中的 SelfUnregModules 動作之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                             |
|-------|--------------------------------------------------------|
| \[1\] | 未註冊的模組檔案識別碼。                |
| \[2\] | 持有未註冊模組檔案的資料夾識別碼。 |



 

## <a name="remarks"></a>備註

SelfUnregModules 動作會嘗試呼叫要取消註冊之模組的 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 函式。 當以較高的許可權執行安裝時，此動作會以較高的許可權執行，例如在個別電腦安裝期間。 在每一使用者安裝期間，安裝程式會以使用者權限執行此動作。

請注意，您不能指定安裝程式使用 SelfUnRegModules 動作來取消註冊 Dll 的順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定自我註冊的順序](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
