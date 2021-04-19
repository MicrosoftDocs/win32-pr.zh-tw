---
description: 網路監視器包含下列 BLOB 函數。
ms.assetid: 90514067-59e9-4bd9-8612-2263bd414574
title: BLOB 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a059e997a06d3295f598d65956c62d06953767ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979131"
---
# <a name="blob-functions"></a>BLOB 函數

網路監視器包含下列 BLOB 函數。



| 函式                                                       | 描述                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [CreateBlob](createblob.md)                                   | 建立空的 BLOB。                                                                                                           |
| [CreateNPPInterface](createnppinterface.md)                   | 建立具有指定 BLOB 的 NPP 介面。                                                                                      |
| [DestroyBlob](destroyblob.md)                                 | 釋出與指定 BLOB 相關聯的所有記憶體。                                                                                   |
| [DuplicateBlob](duplicateblob.md)                             | 複製指定的 BLOB。                                                                                                             |
| [GetBoolFromBlob](getboolfromblob.md)                         | 從指定的 BLOB 抓取已命名的布林值。                                                                             |
| [GetClassIDFromBlob](getclassidfromblob.md)                   | 從指定的 BLOB 抓取命名的類別識別碼值。                                                                    |
| [GetDwordFromBlob](getdwordfromblob.md)                       | 從指定的 BLOB 抓取指名的 **DWORD** 值。                                                                           |
| [GetMacAddressFromBlob](getmacaddressfromblob.md)             | 從指定的 BLOB 抓取指名的 MAC 位址。                                                                               |
| [GetNetworkInfoFromBlob](getnetworkinfofromblob.md)           | 從指定的 BLOB 抓取網路資訊。                                                                                 |
| [GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md) | 從指定的 BLOB 抓取位址篩選資訊。                                                                          |
| [GetNPPBlobFromUI](getnppblobfromui.md)                       | 顯示 [ **選取網路** ] 對話方塊，並傳回所選 NIC 的 NPP BLOB。                                       |
| [GetNPPBlobTable](getnppblobtable.md)                         | 捕獲 Blob 的資料表。                                                                                                      |
| [GetNPPEtypeSapFilter](getnppetypesapfilter.md)               | 從指定的 BLOB 抓取 Etype/Sap 篩選器。                                                                                |
| [GetNPPMacTypeAsNumber](getnppmactypeasnumber.md)             | 從 NPP 區段的 **NetworkInfo** 類別中抓取 mac 類型，並將資訊轉換成 MAC 類型號碼。 |
| [GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md) | 從指定的 BLOB 抓取模式比對篩選。                                                                            |
| [GetNPPTriggerFromBlob](getnpptriggerfromblob.md)             | 抓取指定 BLOB 的觸發程式。                                                                                           |
| [GetStringFromBlob](getstringfromblob.md)                     | 從指定 BLOB 內的特定位置抓取單一字串。                                                          |
| [GetStringsFromBlob](getstringsfromblob.md)                   | 從指定的 BLOB 抓取指定界限內的所有字串。                                                          |
| [IsRemoteNPP](isremotenpp.md)                                 | 指出指定的 BLOB 是否指定遠端 NPP。                                                                         |
| [MergeBlob](mergeblob.md)                                     | 合併來源和目標 Blob 中的資訊，並以來源 BLOB 的資料覆寫一般專案。                  |
| [RegCreateBlobKey](regcreateblobkey.md)                       | 將 BLOB 儲存在指定的登錄機碼上。                                                                                         |
| [RegOpenBlobKey](regopenblobkey.md)                           | 抓取儲存在指定登錄機碼的 BLOB。                                                                               |
| [RemoveFromBlob](removefromblob.md)                           | 從指定 BLOB 的任何層級移除資訊。                                                                              |
| [SelectNPPBlobFromTable](selectnppblobfromtable.md)           | 從資料表中選取 NPP 的 BLOB。                                                                                                |
| [SetBoolInBlob](setboolinblob.md)                             | 設定 BLOB 內指定位置的布林值。                                                                        |
| [SetClassIDInBlob](setclassidinblob.md)                       | 設定 BLOB 的命名類別識別碼值。                                                                                |
| [SetDwordInBlob](setdwordinblob.md)                           | 設定 BLOB 的命名 **DWORD** 值。                                                                                       |
| [SetMacAddressInBlob](setmacaddressinblob.md)                 | 設定 BLOB 的命名 MAC 位址。                                                                                           |
| [SetNetworkInfoInBlob](setnetworkinfoinblob.md)               | 設定 BLOB 的網路資訊。                                                                                         |
| [SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)     | 在 BLOB 中設定指定的位址篩選準則。                                                                                       |
| [SetNPPEtypeSapFilter](setnppetypesapfilter.md)               | 設定 BLOB 中的 Etype/Sap 篩選器。                                                                                             |
| [SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)     | 設定 BLOB 的模式比對篩選。                                                                                        |
| [SetNPPTriggerInBlob](setnpptriggerinblob.md)                 | 設定 BLOB 中的觸發程式。                                                                                                      |
| [SetStringInBlob](setstringinblob.md)                         | 設定 BLOB 內指定位置的字串。                                                                               |
| [WriteBlobToFile](writeblobtofile.md)                         | 將 BLOB 寫入至指定的檔案。                                                                                                   |



 

 

 



