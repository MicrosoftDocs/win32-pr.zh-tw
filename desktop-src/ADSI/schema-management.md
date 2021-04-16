---
title: 架構管理
description: ADSI 範例提供者元件定義了架構類別 \ 0034; 組織單位 \ 0034;和 \ 0034;使用者 \ 0034;然後以下列方式管理這些架構類別。
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- 架構管理 ADSI
- 架構管理 ADSI
- 管理架構 ADSI
- 架構，管理 ADSI
- 管理架構 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104571460"
---
# <a name="schema-management"></a>架構管理

ADSI 範例提供者元件會定義架構類別「組織單位」和「使用者」，並以下列方式管理這些架構類別。

「組織單位」架構類別是以 ADs 容器物件表示，並可包含其他「組織單位」和「使用者」。 容器物件支援介面 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)、 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)和 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)。 "User" 架構類別是以泛型 Active Directory 物件表示，而不包含其他類型的物件。 在範例提供者元件中，使用者物件會實作為支援介面 **IUnknown**、 **IDispatch** 和 **IADs** 的泛型 Active Directory 物件。 請注意，在此案例中，使用者物件不支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面。

範例提供者元件也必須執行 ADs 命名空間物件，此物件支援介面 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)、 [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。

下圖顯示表示兩個範例提供者元件架構類別的架構詳細資料。

![adsi 範例提供者元件架構](images/dssmsch.png)

請注意，在上圖中，「組織單位」架構類別會定義三個屬性： "Description"、"Headcounts" 和 "ID"。 「使用者」架構類別定義四個屬性：「識別碼」、「名稱」、「PhoneNumber」和「標題」。 這兩個架構類別都會共用 "ID" 屬性。 每個屬性都是由 "String" 或 "Integer" 語法物件所定義。

> [!Note]  
> 範例提供者元件的第一個版本中不會有語法物件。 不過，在大部分的 Microsoft ADSI 架構中，語法物件都會包含在架構容器物件中，就像架構類別和屬性物件一樣。 基於這個理由，它們會顯示在這裡。

 

此提供者元件可讓 ADSI 用戶端應用程式以 ADs 類別物件、ADs 屬性物件和 ADs 語法物件的形式存取架構資料，而這一切都是在架構類別容器物件內，以便在執行時間抓取架構資料。

為範例提供者元件定義的架構類別容器物件的 ADsPaths 是 "Sample://Seattle/schema" 和 "Sample://Toronto/schema"。 在此範例中，架構的內容相同。

 

 