---
description: IUpdateCollection 介面會定義下列屬性。
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: IUpdateCollection 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859758"
---
# <a name="iupdatecollection-properties"></a>IUpdateCollection 屬性

[**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)介面會定義下列屬性。



| 屬性                                        | 描述                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | 取得可用來列舉集合的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 |
| [**計數**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | 取得集合中的項目數。                                                                           |
| [**項目**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | 取得或設定集合中的 [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) 介面。                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | 取得布林值，這個值表示更新集合是否為唯讀。                                          |



 

 

 
