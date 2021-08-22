---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: 'P (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230d3dba8be620b0d2d473dbf23960fff79cb7c76abc8a686c47a630605318d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050786"
---
# <a name="p-wmi"></a>P (WMI) 

[B](gloss-a.md) [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**效能計數器**
</dt> <dd>

性能類別中的屬性，此屬性衍生自儲存效能資料的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 。

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**效能物件**
</dt> <dd>

效能程式庫中的物件，可將資料儲存在計數器中。 這些物件會顯示在 [*系統監視器*](gloss-s.md) 公用程式中。 範例包括 Cache 和 Logical Disk 物件。 由 [*ADAP*](gloss-a.md) 進程傳送至 WMI 時，每個物件都會變成兩個 WMI 效能類別。 一個包含原始資料的類別，衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)。 另一個類別衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ，且包含在系統監視器中可見的相同資料，如同處理後計數器提供者所計算。

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**永久取用者**
</dt> <dd>

其註冊會一直持續到被明確取消為止的 [*事件取用者*](gloss-e.md) 。 另請參閱 [*暫時取用者*](gloss-t.md)。

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**實體取用者**
</dt> <dd>

由 [*事件*](gloss-e.md)取用者提供者所執行的 COM 物件，其中包含接收事件通知 [*的接收。*](gloss-s.md)

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**財產**
</dt> <dd>

描述類別資料單位的名稱/值組。 屬性值必須具有有效的 [*受控物件格式 (MOF)*](gloss-m.md) 資料類型。 另請參閱 [*參考屬性*](gloss-r.md)。

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**屬性提供者**
</dt> <dd>

支援對 WMI 屬性進行抓取和修改的 COM 伺服器。 屬性提供者會執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 介面。

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**供應商**
</dt> <dd>

與受管理物件通訊以存取資料和事件通知（例如登錄或 SNMP 裝置）的 COM 伺服器。 提供者將此資料轉送至 [*CIM 物件管理員*](gloss-c.md) ，以進行整合和轉譯。

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**提供者方法**
</dt> <dd>

WMI *提供者* 所實行的方法。

</dd> </dl>

 

 
