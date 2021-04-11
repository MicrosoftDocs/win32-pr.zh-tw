---
description: QueryCoNtextAttributes (Digest) 函數會提供有關安全性內容目前設定的資訊。
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: 查詢摘要資訊安全內容屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944140"
---
# <a name="querying-digest-security-context-attributes"></a>查詢摘要資訊安全內容屬性

[**QueryCoNtextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)函數會提供有關 [*安全性內容*](../secgloss/s-gly.md)目前設定的資訊。

Microsoft Digest 支援查詢下列安全性內容屬性。



| 屬性                   | 描述                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECPKG \_ ATTR 索引 \_ 鍵 \_ 資訊     | 使用中簽署和加密演算法的相關資訊。                                                                                                                                   |
| SECPKG \_ ATTR \_ 套件 \_ 資訊 | 關於 Microsoft Digest 的一般資訊，例如 [*安全性套件*](../secgloss/s-gly.md)所允許的權杖大小上限。 |
| SECPKG \_ ATTR \_ 大小         | 訊息相關資料（例如簽章）所允許的大小上限。                                                                                                                                |



 

 

 
