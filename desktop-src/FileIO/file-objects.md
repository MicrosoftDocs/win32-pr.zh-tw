---
description: 檔案物件可作為核心和使用者模式進程之間的邏輯介面，以及位於實體磁片上的檔案資料。
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: File 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263eae282f76195cc125848f13f43f5ee3d8f676cc6328b2d03db443e6f1deec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107468"
---
# <a name="file-objects"></a>File 物件

檔案 *物件* 可作為核心和使用者模式進程之間的邏輯介面，以及位於實體磁片上的檔案資料。 File 物件包含寫入檔案的資料，以及下列一組核心維護的屬性。



| 資訊類型                                              | 目的                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 檔案名稱                                                     | 為對應的實體檔案命名。                                                                                                                                                          |
| 目前位元組位移                                           | 用於同步檔案 i/o (本節稍後所述) 識別讀取和寫入作業目前的開始位置。                                                          |
| 共用模式                                                    | 指定第二個進程是否可以在初始進程仍在存取時，開啟檔案以進行讀取、寫入或刪除存取。                                                           |
| I/o 模式                                                      | 指定初始進程是否開啟檔案以進行 [同步或非同步 i/o](synchronous-and-asynchronous-i-o.md)、快取或未快取 i/o、連續或隨機 i/o 等等。 |
| 裝置物件的指標                                      | 識別檔案資料所在的實體裝置。                                                                                                                                        |
| 磁片區參數區塊的指標，或 [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | 識別檔案資料所在的磁片區或磁碟分割。                                                                                                                                    |
| 區段物件指標的指標                            | 識別描述 [對應](/windows/desktop/Memory/file-mapping)檔案的根結構。                                                                                                                  |
| 私人快取對應的指標                                  | 識別目前快取的檔案資料。                                                                                                                                              |



 

在 Ntddk 中，這些屬性會定義為 [**FILE \_ 物件**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) 結構的一部分。 請參閱 Windows 驅動程式套件 (WDK) 檔中此結構的定義，以瞭解值的資料長度和類型。

 

 
