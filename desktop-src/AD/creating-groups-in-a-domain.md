---
title: 在網域中建立群組
description: 在將包含新群組的網域容器 Active Directory Domain Services 中建立群組物件。
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- 群組 AD，在網域中建立群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023266"
---
# <a name="creating-groups-in-a-domain"></a>在網域中建立群組

在將包含新群組的網域容器 Active Directory Domain Services 中建立群組物件。 您可以在網域的根目錄、組織單位內或在容器內建立群組。 若要建立群組物件，請使用 [**IADsContainer：： create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 或 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) 方法。

需要下列屬性才能讓群組物件成為 Active Directory 伺服器和 Windows 安全性系統可辨識的合法群組：

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**快遞 之 家**
</dt> <dd>

指定目錄中群組物件的名稱。 這會是在建立群組的容器內，物件的相對辨別名稱。

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

包含指定群組類型和範圍的整數。 [**ADS \_ 群組 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)列舉會定義 **groupType** 屬性的可能值。

下列清單會定義此屬性的一般群組類型和值。

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>網域本機散發
</dt> <dd>

**ADS \_ 群組 \_ 類型 \_ 域 \_ 本地 \_ 組**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>網域區域安全性
</dt> <dd>

**廣告 \_群組 \_ 類型的 \_ 網域 \_ 本地 \_ 組** \| **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>全域散發
</dt> <dd>

**ADS \_ 群組 \_ 類型 \_ 全域 \_ 群組**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>全域安全性
</dt> <dd>

**廣告 \_群組 \_ 類型 \_ 全域 \_ 群組** \| **廣告 \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>通用散發
</dt> <dd>

**ADS \_ 群組 \_ 類型 \_ 通用 \_ 組**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>通用安全性
</dt> <dd>

**廣告 \_群組 \_ 類型 \_ 通用 \_ 群組** \| **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**

</dd> <dt>


</dt> <dd>

</dd> </dl>

如果群組是要在目錄物件上設定存取控制，則群組應該是全域安全性或通用安全性群組。

請注意，通用安全性群組只能建立在以原生模式執行的 Windows 2000 網域上。 如需偵測混合和原生模式的詳細資訊，請參閱偵測 [網域的操作模式](detecting-the-operation-mode-of-a-domain.md)。

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

包含字串，此字串是用來支援舊版用戶端和伺服器的名稱。 **SAMAccountName** 應小於20個字元，以支援舊版 Windows 的用戶端。

**SAMAccountName** 在網域內的所有安全性主體物件之間必須是唯一的。 應針對定義域執行查詢，以確認 **sAMAccountName** 在網域內是唯一的。

</dd> </dl>

您可以使用 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) 方法，在建立時加入群組的成員。 您可以選擇性地使用 [**IADsGroup：： Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) 方法，在建立之後將成員新增至群組。 如需有關將成員新增至群組的詳細資訊，請參閱 [將成員新增至網域中的群組](adding-members-to-groups-in-a-domain.md)。

 

 