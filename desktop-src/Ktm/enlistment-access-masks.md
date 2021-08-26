---
description: KTM 會定義下列登記存取遮罩，以在開啟登記時使用。
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: '登錄存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870108"
---
# <a name="enlistment-access-masks"></a>登記存取遮罩

KTM 會定義下列登記存取遮罩，以在開啟登記時使用。

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**登記 \_ 查詢 \_ 資訊**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



呼叫者可以查詢 KTM 以取得登記的相關資訊。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**登記 \_ 設定 \_ 資訊**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



呼叫端可以設定登記的相關資訊。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**登記 \_ 復原**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



呼叫端可以復原登記。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**登記 \_ 次級 \_ 許可權**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



呼叫端可以完成資源管理員代表交易執行的動作。 以下是動作的清單：

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**登記 \_ 優異 \_ 許可權**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



呼叫端可以在交易中登記為高階交易管理員。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**登記 \_ 一般 \_ 讀取**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取** 和 **登記 \_ 查詢 \_ 資訊**。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**登記 \_ 一般 \_ 寫入**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 寫入**、登錄 **\_ 集 \_ 資訊** 和 **登記 \_ 復原**。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**登記 \_ 泛型 \_ 執行**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**、 **登記 \_ 復原** 和 **登記 \_ 次級 \_ 許可權**。


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**登記 \_ 所有 \_ 存取**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



此值會設定登記存取值的所有有效位。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                           |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinNT。h</dt> </dl> |



 

 




