---
title: CENUMOBJ.Cpp
description: 在範例提供者元件中，容器物件的列舉會使用下表所列的 cenumobj 中的常式。
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683081"
---
# <a name="cenumobjcpp"></a>CENUMOBJ.Cpp

在範例提供者元件中，容器物件的列舉會使用下表所列的 cenumobj 中的常式。



| 方法                                                 | 描述                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum：： Create**                     | 建立物件，以啟用泛型 Active Directory 物件的列舉。                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | 初始化。                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | 管理物件的抓取。                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | 取出符合篩選準則的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標集合。                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | 取得物件，並比對篩選。 如果相符，請將其包裝在泛型物件中，並傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | 管理物件的取出。                                                                                                                                        |
| **CSampleDSGenObjectEnum：： Next**                       | 從指出的列舉物件取出指定的元素數目。                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | 確認物件類別符合篩選清單中的一個。                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | 管理篩選陣列。                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | 將新的物件類別加入至篩選，並將篩選準則設定為連續。                                                                                                |
| **FreeFilterList**                                     | 釋放篩選。                                                                                                                                                      |



 

 

 