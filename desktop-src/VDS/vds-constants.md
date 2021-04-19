---
description: VDS 常數
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: VDS 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981040"
---
# <a name="vds-constants"></a>VDS 常數

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

VDS 常數的分類方式如下：

-   [物件狀態常數](#object-status-constants)
-   [Automagic 提示常數](#automagic-hints-constants)
-   [其他常數](#miscellaneous-constants)

### <a name="object-status-constants"></a>物件狀態常數



| 常數           | 值 |
|--------------------|-------|
| 狀態 \_ 不明    | 0     |
| \_線上狀態     | 1     |
| 狀態 \_ 未 \_ 就緒 | 2     |
| 狀態 \_ 沒有 \_ 媒體  | 3     |
| \_離線狀態    | 4     |
| 狀態 \_ 失敗     | 5     |
| 狀態 \_ 遺失    | 6     |



 

### <a name="automagic-hints-constants"></a>Automagic 提示常數



| 常數                               | 值   |
|----------------------------------------|---------|
| VDS \_ 提示 \_ MOSTLYREADS                 | 0x0002L |
| VDS \_ 提示 \_ OPTIMIZEFORSEQUENTIALREADS  | 0x0004L |
| VDS \_ 提示 \_ OPTIMIZEFORSEQUENTIALWRITES | 0x0008L |
| VDS \_ 提示 \_ REMAPENABLED                | 0x0020L |
| VDS \_ 提示 \_ WRITETHROUGHCACHINGENABLED  | 0x0040L |
| VDS \_ 提示 \_ HARDWARECHECKSUMENABLED     | 0x0080L |
| VDS \_ 提示 \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>其他常數



| 常數                     | 值      |
|------------------------------|------------|
| VDS \_ 重建 \_ 優先順序 \_ 下限  | 0x0001L    |
| VER \_ VDS \_ LUN \_ 資訊   | 1          |
| 最大 \_ COMPUTERNAME \_ 長度    | 15         |
| 最大 \_ PROVIDERNAME \_ 長度    | 200        |
| 最大 \_ VERSIONSTRING \_ 長度   | 16         |
| 磁碟機 \_ 號 \_ 的          | N/A        |
| 最大 \_ FS \_ 名稱 \_ 大小          | 8          |
| 不正確 \_ 成員 \_ IDX         | 0xFFFFFFFF |
| GPT \_ 磁碟分割 \_ 名稱 \_ 長度 | 36         |
| 最大 \_ 路徑                    | 260        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 參考](vds-reference.md)
</dt> </dl>

 

 
