---
description: IPv6 的 IPSec 原則和安全性關聯的設定是使用 Ipsec6.exe 完成。
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989912"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

IPv6 的 IPSec 原則和安全性關聯的設定是使用 Ipsec6.exe 完成。 以下是 Ipsec6.exe 子命令：

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_介面_*_\]_*
</dt> <dd>

顯示作用中的安全性原則。 或者，會顯示特定介面的作用中安全性原則。

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**
</dt> <dd>

顯示作用中的安全性關聯。

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_沒有副檔名的檔案名 ()_*_\]_*
</dt> <dd>

建立用來設定安全性原則和安全性關聯的檔案。 建立安全性原則和 *檔案名* 為 Spd 的 *檔案名*。如果是安全性關聯，則為悲傷。 使用已建立的檔案做為範本，以設定安全性原則或安全性關聯。 您可以使用文字編輯器來修改檔案。 若要叫用包含在 SPD 和悲傷檔案中的設定，請使用 **ipsec6** 命令。

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[**_沒有副檔名的檔案名 ()_*_\]_*
</dt> <dd>

將 *檔案名中* 的安全性原則（副檔名為 spd 和安全性關聯）新增至有效的安全性原則和安全性關聯 *清單。*

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[** *_原則 \] 檔案名 \[_* _(沒有副檔名)_*_\]_*
</dt> <dd>

將 filename 中的安全性原則和 *檔案名**中的* 安全性關聯新增至 active 安全性原則和安全性關聯的清單，如原則編號所參考。

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ type = sp sa \] \[** _IndexNumber_*_\]_*
</dt> <dd>

會從作用中的安全性原則和安全性關聯清單中刪除安全性原則或安全性關聯， (使用 **ipsec6 sp** 或 **ipsec6 sa**) 來顯示它們的索引編號。

</dd> </dl>

 

 



