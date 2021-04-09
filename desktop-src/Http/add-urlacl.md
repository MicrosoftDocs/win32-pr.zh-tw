---
title: add urlacl
description: 保留非系統管理員使用者和帳戶的指定 URL。
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- 新增 urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103946033"
---
# <a name="add-urlacl"></a>add urlacl

保留非系統管理員使用者和帳戶的指定 URL。 您可以使用帳戶名稱搭配接聽和委派參數，或使用安全描述項定義語言 (SDDL) 字串，來指定任意的存取控制清單 (DACL) 。

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url =] 字串**
</dt> <dd>

指定完整的 URL。

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[使用者 =] 字串**
</dt> <dd>

指定使用者或使用者組名。

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[接聽 = {yes \| 否}\]**
</dt> <dd>

指定下列其中一個值：

-   是：允許使用者註冊 Url。 這是預設值。
-   否：拒絕使用者註冊 Url。

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate = {yes \| 否}\]**
</dt> <dd>

指定下列其中一個值：

-   是：允許使用者委派 Url。
-   否：拒絕使用者委派 Url。 這是預設值。

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl =] 字串**
</dt> <dd>

指定描述 DACL 的 SDDL 字串。

</dd> </dl>

## <a name="examples"></a>範例

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>另請參閱

* [Netsh http 命令](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 