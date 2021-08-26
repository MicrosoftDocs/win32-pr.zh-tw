---
description: MsiSFCBypass 資料表包含檔案的清單，這些檔案應在 Microsoft Windows Me 上安裝檔案時略過 Windows 檔案保護。
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: MsiSFCBypass 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d233f09aa62b5f6d17112b1f5a98753e328f3a1746c452de5a5a1689a36f971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042668"
---
# <a name="msisfcbypass-table"></a>MsiSFCBypass 資料表

MsiSFCBypass 資料表包含檔案的清單，這些檔案應在 Microsoft Windows Me 上安裝檔案時略過 Windows 檔案保護。

MsiSFCBypass 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 檔案\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

檔案[資料表](file-table.md)的外鍵，指定當檔案安裝在 Windows Me 時，應略過 Windows 檔案保護的檔案。

</dd> </dl>

 

 



