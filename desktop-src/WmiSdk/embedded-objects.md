---
description: 内嵌物件是類別的物件，存在於另一個類別的類別或實例宣告內。
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: 在類別中內嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979965"
---
# <a name="embedding-objects-in-a-class"></a>在類別中內嵌物件

内嵌物件是類別的物件，存在於另一個類別的類別或實例宣告內。 例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別包含 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的内嵌物件。 每個 **win32 \_ 信任** 物件都包含一個 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件。 WMI 不會限制類別可以有内嵌物件的深度。 不過，使用另一個設計（例如建立關聯類別）可能會讓架構更容易管理。

如需有關内嵌物件的詳細資訊，請參閱下列主題：

-   [建立内嵌物件](creating-embedded-objects.md)
-   [查詢内嵌物件](querying-embedded-objects.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
