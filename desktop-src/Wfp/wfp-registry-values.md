---
description: WFP 登錄值位於下列登錄機碼中： HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon。
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: WFP 登錄值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996940"
---
# <a name="wfp-registry-values"></a>WFP 登錄值

\[Windows Vista 不支援 WFP 登錄值。\]

WFP 使用數個登錄值進行自訂設定。 WFP 登錄值位於下列登錄機碼中：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

以下是 WFP 登錄值。

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

快取的位置。 這必須是本機路徑。 預設值為% systemroot% \\ system32 \\ dllcache。

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

配額選項。 此登錄值可以是下列其中一個值。



| 值                  | 意義                                                  |
|------------------------|----------------------------------------------------------|
| SFC \_ 配額 \_ 所有 \_ 檔案 | DLL 快取的大小不受限制。 此為預設值。 |
| 其他值           | DLL 快取的大小，以檔案為限。                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

掃描選項。 此登錄值可以是下列其中一個值。



| 值             | 意義                                                   |
|-------------------|-----------------------------------------------------------|
| SFC \_ 掃描 \_ 正常 | 請勿在開機時掃描受保護的檔案。 此為預設值。 |
| \_一律掃描 \_ SFC | 在每次開機時掃描受保護的檔案。                       |
| SFC \_ 掃描 \_ 一次   | 在下一次開機時掃描受保護的檔案。                    |



 

</dd> </dl>

 

 



