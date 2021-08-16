---
title: 通用類別目錄
description: Active Directory Domain Services 所執行的網域可包含許多分割區或命名內容。
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- 通用類別目錄 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189111"
---
# <a name="global-catalog"></a>通用類別目錄

Active Directory Domain Services 所執行的網域可包含許多分割區或命名內容。 物件的分辨名稱 (DN) 包含足夠的資訊，以找出保存物件之分割區的複本。 但是，使用者或應用程式不知道目標物件的 DN，或哪個分割區可能包含物件。 [*通用類別目錄 (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85))可讓使用者和應用程式在指定目標物件的一或多個屬性的 Active Directory 域樹中尋找物件。

通用類別目錄包含目錄中每個命名內容的部分複本。 它也包含架構和設定命名內容。 這表示 GC 會保存目錄中每個物件的複本，但只有少數屬性。 GC 中的屬性是搜尋作業中最常使用的屬性 (例如使用者的名字和姓氏，或登入名稱) ，以及找出物件完整複本所需的屬性。 GC 可讓使用者快速找出感興趣的物件，而不需要知道有哪些網域保存這些物件，而不需要在企業中使用連續的延伸命名空間。

通用類別目錄是由 Active Directory Domain Services 複寫系統自動建立。 系統會自動產生通用類別目錄的複寫拓撲。 複寫到通用類別目錄的屬性包含由 Microsoft 定義的基底集合。 系統管理員可以指定其他屬性，以符合其安裝的需求。

 

 