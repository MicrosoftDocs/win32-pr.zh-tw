---
description: 通知類型宏包含下列元素。
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: 通知類型宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e50146d6a6fc71cc78baccd97a7dffc9e4ed4e7091373dd52ae42b2fbc6b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992738"
---
# <a name="notification-type-macro"></a>通知類型宏

通知類型宏包含下列元素。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

## <a name="components"></a>單元

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>物件描述元
</dt> <dd>

將名稱附加至通知類型宏中的 SNMP 事件。 下列清單列出對應物件描述項的規則。



| 類型                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 封裝的 CIM 類別名稱 | 「SNMP \_ 」<br/> MIB 模組身分識別名稱<br/> 底線 (\_) <br/> 物件描述元<br/> 「 \_ 通知」<br/> 範例：來自 **CISCO-VTP-MIB** 的 **vtpServerDisabled** 通知會對應到 **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ 通知**。<br/>                 |
| 引用 CIM 類別名稱     | 「SNMP \_ 」<br/> MIB 模組身分識別名稱<br/> 底線 (\_) <br/> 物件描述元<br/> " \_ ExtendedNotification"<br/> 範例：來自 **CISCO-VTP-MIB** 的 **vtpServerDisabled** 通知會對應到 **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**。<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS 子句
</dt> <dd>

列舉與通知物件相關聯的物件集合。

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE 子句
</dt> <dd>

指的是包含物件之詳細資訊的另一份檔。 它會對應到 CIM 類別限定詞 **參考**，它是字串類型。

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION 子句
</dt> <dd>

描述有問題的物件。 它會對應至 CIM 類別限定詞 **描述**，其為字串類型

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS 子句
</dt> <dd>

指出是否必須支援此物件。 當狀態為「已 **淘汰** 」 **或「已淘汰」** 時，會從對應中捨棄通知。 否則，此子句會對應到 CIM 類別限定詞 **狀態**，其為 **字串** 類型。

針對 SNMPv1，[ **狀態** ] 的慣用值是 [ **強制** ] 或 [ **選擇性**]，但辨識符號可以包含其他一些值。 若為 SNMPv2C，則 [ **狀態** ] 的慣用值為 [ **目前** ] 或 [已 **淘汰**]，但辨識符號可以包含其他一些值。

</dd> </dl>

## <a name="remarks"></a>備註

SNMP 提供者會將 **通知類型** 宏對應至已封裝或引用的類別定義。

封裝的類別定義不會公開與 MIB 物件相關聯的實例資訊。 相反地，類別定義會將 OBJECTS 子句編碼為 CIM 事件類別的一連串屬性。 每個 CIM 屬性都會反映 OBJECTS 子句中對應 MIB 物件的名稱、類型和值。 如果您需要實例資訊，則必須對應至引用類別。 封裝的類別定義會對應至 [SnmpNotification](snmpnotification.md) 類別。

引用類別會定義 MIB 物件，以及用來取得物件的實例資訊。 類別定義會將 OBJECTS 子句編碼為 CIM 事件類別的一連串屬性。 每個 CIM 屬性都會反映 OBJECTS 子句中對應的 MIB 物件的名稱，而類型則會反映與該 MIB 物件相關聯之類別實例的内嵌物件。 然後，提供者會產生與 MIB 物件相關聯的類別。 例如， **ifIndex** 會對應到名為 **SNMP \_ RFC1213 \_ MIB \_ ifIndex** 的內嵌類別。 如需這種類別類別的詳細資訊，請參閱 [OBJECT Type 宏](object-type-macro.md)。

 

 




