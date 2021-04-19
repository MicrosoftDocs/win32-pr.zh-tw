---
title: CENUMNS.Cpp
description: 在範例提供者元件中，命名空間物件的列舉會使用下表所列 cenumns 中的方法。
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969535"
---
# <a name="cenumnscpp"></a>CENUMNS.Cpp

在範例提供者元件中，命名空間物件的列舉會使用下表所列 cenumns 中的方法。



| 方法                                              | 描述                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum：： Create**                  | 建立物件，以允許列舉 ADS 命名空間物件。                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | 標準的函式。                                                                                                                                     |
| **CSampleDSNamespaceEnum：： ~ CSampleDSNamespaceEnum** | 標準的函式。                                                                                                                                      |
| **CSampleDSNamespaceEnum：： Next**                    | 從指定的命名空間物件取出指定的元素數目。                                                                            |
| **CSampleDSNamespaceEnum：： EnumObjects**             | 管理物件介面指標的取出。                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | 提取 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標集合。                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | 提取下一個物件。 如果找到，請建立泛型 Active Directory 物件並取出其 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 |



 

 

 