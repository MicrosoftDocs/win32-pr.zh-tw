---
title: /系統交換器
description: /系統參數會指示 MIDL 編譯器為指定的系統產生類型程式庫。 預設值為目前的作業系統。
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /系統交換器 MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31def6297a1a91f6ed28943290a66b544dc368d5a00a91932035a338af50bac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643776"
---
# <a name="system-switch"></a>/<system> 開關

此 **/<system>** 參數會指示 MIDL 編譯器為指定的系統產生類型程式庫。 預設值為目前的作業系統。

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32 * * * *


</dt> <dd>

Windows 2000、Windows XP、Windows Vista Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Intel 架構的64位 Windows 環境，例如 Windows 2000、Windows Server 2003、Windows XP Professional x64 Edition、Windows Vista 或 Windows 7。

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

以美國微裝置為基礎的64位 Windows 環境，例如 Windows 2000、Windows Server 2003、Windows XP Professional x64 Edition、Windows Vista 或 Windows 7。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**/<system>** 參數的功能與 midl [**/env**](-env.md)選項相同，而且 midl 編譯器只會針對回溯相容性與 mktyplib.exe 進行辨識。 如果您要產生新的 makefile，請使用 **/env** 參數。

## <a name="examples"></a>範例

**midl/win32 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




