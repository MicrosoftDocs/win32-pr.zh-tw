---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: " (WMI) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7089d3b4e7714b84dc02f6491da1c0a8d21d1b83c1729ac9fe04824c83a6789e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993188"
---
# <a name="s-wmi"></a> (WMI) 

[B](gloss-a.md) [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**模式**
</dt> <dd>

類別定義的集合，描述特定環境中的 [*managed 物件*](gloss-m.md) 。

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**安全描述項**
</dt> <dd>

包含安全物件安全性資訊（例如共用、檔案、接收或事件篩選器）的資料結構。

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**(SID) 的安全識別碼**
</dt> <dd>

識別使用者、群組和電腦帳戶的資料結構。

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**半同步**
</dt> <dd>

請參閱 *半同步方法*。

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**半同步**
</dt> <dd>

請參閱 *半同步方法*。

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**半同步方法**
</dt> <dd>

立即傳回並讓應用程式或腳本將傳回的物件列舉為集合的方法呼叫。

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**服務 SID**
</dt> <dd>

針對每個安全性內容建立的唯一 *SID* ;也就是「LocalService」，另一個用於「NetworkService」。 只有 *服務 SID* 具有資源（例如執行緒和事件）的許可權，這些資源是由 WMI 提供者主機進程 (wmiprvse.exe) 所建立。

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**希**
</dt> <dd>

請參閱 *安全性識別* 元。

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**singleton 類別**
</dt> <dd>

支援單一實例的 WMI 類別。

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**下沉**
</dt> <dd>

COM 物件，作為非同步作業結果或事件通知的實體傳遞目的地。 由 [*永久取用者*](gloss-p.md) 所執行的接收器支援 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 介面。 [*暫時性取用者*](gloss-t.md)所執行的接收，或是進行非同步呼叫的應用程式，都支援 [**IWbemObjectSink**](iwbemobjectsink.md)介面。

腳本用戶端可以使用 [**SWbemSink**](swbemsink.md) 物件和事件（例如 [**OnObjectReady**](swbemsink-onobjectready.md)），來接收非同步呼叫所產生的回呼。

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**標準取用者**
</dt> <dd>

預先安裝的 [*永久取用者*](gloss-p.md) ，會執行動作，例如，在 [*受控物件格式 (MOF)*](gloss-m.md) 檔或腳本設定時傳送電子郵件訊息或寫入記錄檔。

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**標準提供者**
</dt> <dd>

內建于 WMI 的 [*提供者*](gloss-p.md) ，與協力廠商或自訂提供者不同。

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**標準辨識符號**
</dt> <dd>

[*CIM 物件管理員*](gloss-c.md)自動附加至方法之類別、實例、屬性、方法或參數的辨識 [*符號*](gloss-q.md)。

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**標準架構**
</dt> <dd>

共同的概念架構，可組織和關聯代表系統、網路或應用程式目前操作狀態的類別。 [*分散式管理工作強制 (DMTF)*](gloss-d.md)定義 [*通用訊息模型 (CIM)*](gloss-c.md)中的標準架構。

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**靜態類別**
</dt> <dd>

很少會變更的 CIM 類別定義，而且會儲存在 [*cim 存放庫*](gloss-c.md) 中，直到明確刪除為止。 [*CIM 物件管理員*](gloss-c.md)可以提供靜態類別的定義，而不使用 [*提供者*](gloss-p.md)。 靜態類別可支援 *靜態* 或 [*動態實例*](gloss-d.md)。

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**靜態實例**
</dt> <dd>

CIM 類別的實例，這個類別會持續儲存在 [*cim 存放庫*](gloss-c.md) 中，並在明確刪除之前保持有效，甚至是跨系統重新開機。

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**靜態方法**
</dt> <dd>

在 CIM 類別中定義的方法，該方法是藉由抓取類別定義而非抓取類別的實例來執行。

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**ubschema**
</dt> <dd>

特定組織所擁有的 *架構* 部分。 [*Win32schema*](gloss-w.md)是 ubschema 的範例。

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**system 類別**
</dt> <dd>

[*CIM 物件管理員*](gloss-c.md)定義來支援核心功能（例如事件通知、安全性和當地語系化）的類別。 系統會在每個 [*命名空間*](gloss-n.md)中自動定義系統類別。 系統類別衍生自抽象基類 [**\_ \_ SystemClass**](--systemclass.md)。

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**系統監視器**
</dt> <dd>

 (CIM) 公用程式，這是用來監視效能的 GUI。

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**系統屬性**
</dt> <dd>

[*CIM 物件管理員*](gloss-c.md)定義的屬性，以提供適用于每個類別的資訊，例如名稱、衍生和 [*命名空間*](gloss-n.md)。

</dd> </dl>

 

 



