---
description: 磁片區陰影複製 API 中定義了下列資料類型：
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: 磁片區陰影複製 API 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690468"
---
# <a name="volume-shadow-copy-api-data-types"></a>磁片區陰影複製 API 資料類型

磁片區陰影複製 API 中定義了下列資料類型：

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>VSS \_ 識別碼
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

**Vss 識別碼 \_** 定義會指定一般 VSS 識別碼格式。 **VSS \_ 識別碼** 是標準的 GUID 資料類型。

**VSS \_識別碼** 是用來識別下列各項：陰影複製、陰影複製集、提供者、提供者版本、寫入器 (寫入器的類別識別碼) 和寫入器的實例。

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

**VSS \_ PWSZ** 定義會指定以 null 終止的寬字元字串， (wchar) 。

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS \_ 時間戳記
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

**VSS \_ 時間戳記** 定義會將時間戳記資訊保存為64位整數值，其中包含自年1月1日起 1601 (UTC) 的100秒數間隔。 這項定義可與 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構互換。

</dd> </dl>

 

 
