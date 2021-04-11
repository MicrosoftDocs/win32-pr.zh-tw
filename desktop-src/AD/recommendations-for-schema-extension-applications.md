---
title: 架構延伸應用程式的建議
description: 本主題包含架構延伸應用程式的建議。
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- 架構延伸應用程式 AD 的建議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092626"
---
# <a name="recommendations-for-schema-extension-applications"></a>架構延伸應用程式的建議

除了必要條件之外，建議針對架構延伸應用程式使用下列最佳作法：

-   尋找架構主機。 系結至位於架構主機之 DC 上的架構。 避免不必要變更 Dc 之間的架構主機角色。 系結至架構主機上的架構容器。 如需詳細資訊，請參閱 [安裝架構延伸模組的必要條件](prerequisites-for-installing-a-schema-extension.md)。
-   在執行任何動作之前，請檢查架構容器的 **allowedChildClassesEffective** 屬性，以確認您可以建立屬性和/或類別。 如果 **attributeSchema** 和 **classSchema** 不是該屬性中的值，您就沒有足夠的許可權可以將屬性或類別加入至架構。 如需詳細資訊，請參閱 [檢查許可權以建立架構物件的範例程式碼](example-code-for-checking-for-rights-to-create-schema-objects.md)。
-   確定已在架構主機的登錄中正確設定允許的架構更新。 若要建立或設定此值，請在應用程式清除常式中將其還原為其原始狀態。 如需檢查和設定此值的詳細資訊，請參閱 [在架構主機上啟用架構變更](enabling-schema-changes-at-the-schema-master.md)。
-   新增屬性或類別之前，請先確定它們不存在。 如果存在，請確認它們是您要新增的相同屬性或類別，而不是使用與您的屬性或類別不相容之不同語法和屬性的其他人所建立的屬性或類別。

    針對屬性，請查詢 **cn**、 **attributeID**、 **governsID**、 **lDAPDisplayName** 和 **schemaIDGUID** ，以確定尚未使用這些屬性。 如果您將一組連結屬性新增 (一個轉寄連結，) 一個上一頁連結，請確定 **linkID** 尚未使用。 查詢 **governsID** ，因為 (OID) 的物件識別碼在屬性和類別之間必須是唯一的。

    針對類別，請查詢 **cn**、 **governsID**、 **attributeID**、 **lDAPDisplayName** 和 **schemaIDGUID** ，以確保它們尚未使用。 **AttributeID** 的查詢，因為 OID 在類別和屬性之間必須是唯一的。

    如需檢查命名衝突的詳細資訊，請參閱偵測 [架構命名衝突的範例程式碼](example-code-for-detecting-schema-naming-collisions.md)。

    如果有屬性或類別與您的新屬性或類別發生衝突，您的應用程式不應該套用架構變更。

-   如果有這類衝突，您的應用程式不應該套用架構變更。 架構系統管理員可能需要解決衝突，然後再次執行您的應用程式。 或者，您可以使用不同的 **lDAPDisplayName** ;不過，使用屬性或物件的任何應用程式都必須知道該變更。 若要協助避免 OID 衝突，請從 ISO 名稱登錄授權單位取得 OID。
-   如果您的應用程式相依于其已加入的屬性或類別，請先更新架構快取，再加入相依于這些屬性或類別的新屬性或類別。 請注意， **schemaUpdateNow** 操作屬性是同步的。 也就是說， [**IADs：:P**](/windows/desktop/api/iads/nf-iads-iads-put) 的工作區方法呼叫會封鎖，直到更新架構快取為止。 當呼叫傳回時，就會更新架構快取，而且可以存取新的屬性和/或類別。

    如需有關如何更新架構快取的詳細資訊，請參閱更新架構快取的 [範例程式碼](example-code-for-updating-the-schema-cache.md)。

 

 