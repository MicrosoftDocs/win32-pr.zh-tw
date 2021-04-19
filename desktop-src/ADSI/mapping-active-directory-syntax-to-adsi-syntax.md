---
title: 將 Active Directory 語法對應至 ADSI 語法
description: 下表會將 Active Directory 語法對應至其對應的 ADSI 語法。
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- 屬性 ADSI、將 Active Directory 語法對應至 ADSI 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966376"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>將 Active Directory 語法對應至 ADSI 語法

下表會將 Active Directory 語法對應至其對應的 ADSI 語法。



| 屬性語法識別碼 | Active Directory 語法類型             | 相等的 ADSI 語法類型                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | DN 字串<br/>                     | DN 字串<br/>                                                |
| 2.5.5.2<br/>  | 物件識別碼<br/>                     | CaseIgnore 字串<br/>                                        |
| 2.5.5.3<br/>  | 區分大小寫的字串<br/>         | CaseExact 字串<br/>                                         |
| 2.5.5.4<br/>  | 略過 Case 字串<br/>           | CaseIgnore 字串<br/>                                        |
| 2.5.5.5<br/>  | 列印案例字串<br/>             | 可列印字串<br/>                                         |
| 2.5.5.6<br/>  | 數值字串<br/>                | 數值字串<br/>                                           |
| 2.5.5.7<br/>  | **或** 名稱 DNWithOctetString<br/> | 不支援<br/>                                            |
| 2.5.5.8<br/>  | 布林值<br/>                       | 布林值<br/>                                                  |
| 2.5.5.9<br/>  | 整數<br/>                       | 整數<br/>                                                  |
| 2.5.5.10<br/> | 八位字串<br/>                  | 八位字串<br/>                                             |
| 2.5.5.11<br/> | Time<br/>                          | UTC 時間<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Case 忽略字串<br/>                                       |
| 2.5.5.13<br/> | 位址<br/>                       | 不支援<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | NT 安全描述項<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | 大型整數<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | 八位字串<br/>                                             |



 

 

 





