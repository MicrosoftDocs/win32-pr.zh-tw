---
description: 本主題描述可用於準備地區設定識別碼的排序次序識別碼。
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: 排序次序識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320891"
---
# <a name="sort-order-identifiers"></a>排序次序識別碼

本主題描述可用於準備 [地區設定識別碼](locale-identifiers.md)的排序次序識別碼。 排序次序識別碼的定義格式為 " \_ sortorder"，位於識別碼中所使用之地區設定名稱的結尾，例如 "de \_ phoneb"，其中 "phoneb" 是排序次序。 對應的地區設定識別碼的建立方式如下： `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` 。



| 常數                      | 地區設定名稱                                                                                         | 意義                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| 排序 \_ 中文 \_ BIG5           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | 中文 BIG5 順序                                                |
| 排序 \_ 中文 \_ 注音       | zh-隸書 \_ pronun                                                                                       | 繁體中文注音順序                                |
| 排序 \_ 中文 \_ 電話簿 \_    | zh-CN \_ phoneb<br/>                                                                            | 中文 phone book (姓氏) 訂單                                |
| 排序 \_ 中國 \_ 大陸            | zh-CN \_ 筆劃<br/> zh-HK \_ 筆劃<br/> zh-每月 \_ 筆劃<br/> zh-SG \_ 筆劃<br/> | 中國中文筆觸計數順序                                    |
| 排序 \_ 中文 \_ PRCP           | zh-CN<br/> zh-SG<br/>                                                                   | 中國中文拼音順序                                        |
| 排序 \_ 中文 \_ RADICALSTROKE  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | 中文根式/筆劃順序                                      |
| 排序 \_ 中文 \_ UNICODE        | —                                                                                                   | 中文 Unicode order **Windows 2000：** 不支援。<br/>  |
| 排序 \_ 預設值                 | 與對應的語言名稱相同的地區設定名稱                                     | 預設排序次序                                                |
| 排序 \_ 新式格魯吉亞文 \_        | ka-GE \_ 新式                                                                                       | 格魯吉亞文新式順序                                             |
| 排序 \_ 傳統的格魯吉亞文 \_   | ka-GE                                                                                               | 格魯吉亞文傳統順序                                        |
| 排序 \_ 德文的 \_ 電話 \_ 書     | de \_ phoneb                                                                                       | 德文電話書籍訂單                                           |
| 排序 \_ 匈牙利文 \_ 預設值      | hu-HU                                                                                               | 匈牙利文預設順序                                           |
| 排序 \_ 匈牙利文 \_ 技術    | hu-HU \_ technl                                                                                       | 匈牙利文技術訂單                                         |
| 排序 \_ 日文 \_ RADICALSTROKE | ja-JP                                                                                               | 日文的根式/筆劃順序                                     |
| 排序 \_ 日文 \_ UNICODE       | —                                                                                                   | 日文 Unicode 順序 **Windows 2000：** 不支援。<br/> |
| 排序 \_ 日文 \_ XJIS)           | ja-JP                                                                                               | 日文 XJIS) 順序                                               |
| 排序 \_ 韓文 \_ KSC             | ko-KR                                                                                               | 韓文 KSC 訂單                                                  |
| 排序 \_ 韓文 \_ UNICODE         | —                                                                                                   | 韓文 Unicode 順序 **Windows 2000：** 不支援。<br/>   |



 

 

 




