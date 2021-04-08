---
description: 要求編譯器將 MOF 檔案載入至指定為 namespacepath 的命名空間。 如果 MOF 編譯器-n 命名空間參數和 \# pragma 命名空間都&\# 32; namespacepath 命令，則命令優先于參數。
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma 命名空間
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691520"
---
# <a name="pragma-namespace"></a>pragma 命名空間

**Pragma 命名空間** 預處理器命令要求編譯器將 MOF 檔案載入指定為 *namespacepath* 的命名空間。 如果同時使用 MOF 編譯器 **-n** namespace 參數和 **\# pragma namespace** *namespacepath* 命令，則命令優先于參數。

以下說明語法：


```mof
#pragma namespace ("[Namespace]")
```



*\[ 命名 \] 空間* 是指定的命名空間。

如果您未指定此命令或對等的命令列參數，MOF 編譯器預設會使用根 \\ 預設命名空間。

## <a name="remarks"></a>備註

您可以要求用戶端腳本和應用程式使用加密的連接來進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的 mof 檔案。 您也可以藉由新增這個屬性來修改現有的命名空間，然後再次編譯 MOF 檔案。 如需如何使用 **RequiresEncryption** 的詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

## <a name="examples"></a>範例

下列範例示範如何將類別或實例放在「根 \\ 測試」命名空間中。


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[**標準 WMI 限定詞**](standard-wmi-qualifiers.md)
</dt> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 




