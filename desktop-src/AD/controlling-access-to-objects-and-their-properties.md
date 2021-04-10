---
title: 控制物件和其屬性的存取權
description: 若要控制應用程式物件的存取權，請使用物件安全描述項，具體而言，就是使用 (DACL) 及其存取控制 (專案清單) 的任意存取控制清單。
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- 物件 AD，控制存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182959"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>控制物件和其屬性的存取權

若要控制應用程式物件的存取權，請使用物件安全描述項，具體而言，就是使用 (DACL) 及其存取控制 (專案清單) 的任意存取控制清單。

建立物件時，它會接收安全描述項。 如需詳細資訊，以及系統用來為新物件建立 DACL 的規則描述，請參閱 [如何在新的目錄物件上設定安全描述項](how-security-descriptors-are-set-on-new-directory-objects.md)。 這些規則顯示您可以：

-   建立新的安全描述項，並在建立時將其附加至物件。 如需詳細資訊，請參閱 [建立新目錄物件的安全描述項](creating-a-security-descriptor-for-a-new-directory-object.md)。
-   在目錄階層中的任何時間點套用可繼承的 ACE，如此一來，就會將 ACE 繼承到樹狀結構中的物件。 物件可以從其父容器繼承 ACE。 如需詳細資訊，請參閱系統 [管理的繼承與委派](inheritance-and-delegation-of-administration.md)。
-   如果您有必要的存取權限，請在架構中指定預設 DACL 中的 ACE。 架構中的每個物件類別定義都包含預設的安全描述項，可以有預設的 DACL。 如需詳細資訊，請參閱 [預設安全描述項](default-security-descriptor.md)。

此外，您可以修改現有物件的 DACL。 您可以：

-   將 DACL 取代為新的 DACL。
-   讀取現有的 DACL、加以修改，並套用修改過的 DACL。 如需詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

下列清單描述 Active Directory Domain Services 中 ACE 的最重要功能。 您可以使用 ACE：

-   控制可以在物件上執行特定作業的人員。
-   控制誰可以存取物件的特定屬性或屬性集。
-   控制誰可以在容器中建立子物件，包括誰可以建立特定類型的子物件。
-   針對物件類型定義私用控制存取權限，以及控制誰可以執行由私用權利保護的作業。
-   將 ACE 套用至目錄子樹系根目錄中的容器物件，讓樹狀目錄中的所有子物件都能自動繼承保護。
-   套用子樹中的特定子物件類型所自動繼承的 ACE。
-   建立可授與許可權給安全性群組，而不是單一使用者的 ACE。
-   將 ACE 套用至群組原則的物件，以控制受原則影響的帳戶和電腦。

 

 




