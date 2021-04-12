---
description: MsiSFCBypass 資料表所包含的檔案清單，會在檔案安裝在 Microsoft Windows Me 時略過 Windows 檔案保護。
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: MsiSFCBypass 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319911"
---
# <a name="msisfcbypass-table"></a>MsiSFCBypass 資料表

MsiSFCBypass 資料表所包含的檔案清單，會在檔案安裝在 Microsoft Windows Me 時略過 Windows 檔案保護。

MsiSFCBypass 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 檔案\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

檔案 [資料表](file-table.md) 的外鍵，指定當檔案安裝在 windows Me 時應該略過 Windows 檔案保護的檔案。

</dd> </dl>

 

 



