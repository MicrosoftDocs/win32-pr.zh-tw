---
title: 'IP_SPECIFIC_DATA 結構 (Rtm) '
description: IP \_ 特定的資料結構包含 ip 特定的資料。
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA 結構 RAS
- PIP_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 906ae9f2accb3d380227f08ad6b65642b96ce6bfa928591bd11a69c478f531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036668"
---
# <a name="ip_specific_data-structure"></a>IP \_ 特定的 \_ 資料結構

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**Ip \_ 特定的資料** 結構包含 ip 特定的資料。

## <a name="syntax"></a>語法


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**FSD \_ 類型**
</dt> <dd>

指定在 [RFC 1354](routing-protocols-request-for-comments.md)中定義的路由類型。 下表顯示這個成員的可能值。



| 成員                                                                                               | 意義                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 未指定路由類型。 此類型與此處所列的類型不同。<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 路由無效。 通常，這個值會用來使路由失效。 不過，由於路由表管理員不支援失效，因此路由仍會被視為最佳路由計算。 因此，路由通訊協定不應使用此值。<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | 路由是本機路由，也就是下一個躍點是最終目的地。<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 路由是遠端路由，也就是下一個躍點不是最終目的地。<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**FSD \_ 原則**
</dt> <dd>

指定會導致選取多重路徑路由的一組條件。 這個成員通常是採用 IP TOS 格式。 如需詳細資訊，請參閱 [RFC 1354](routing-protocols-request-for-comments.md)。

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

指定下一個躍點的自發系統編號。

</dd> <dt>

**FSD \_ 優先順序**
</dt> <dd>

指定度量值。 路由表管理員會使用此值來比較此路由專案與從其他路由通訊協定取得的路由專案。 此成員的值是由路由表管理員所設定。

</dd> <dt>

**FSD \_ 度量**
</dt> <dd>

指定度量值。 路由表管理員會使用此值，將此路由專案與從相同路由通訊協定取得的其他路由專案進行比較。 此成員的值是由路由通訊協定設定。

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

指定路由通訊協定特定的度量值。 此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。

</dd> <dt>

**FSD \_ Metric2**
</dt> <dd>

指定路由通訊協定特定的度量值。 此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。

</dd> <dt>

**FSD \_ Metric3**
</dt> <dd>

指定路由通訊協定特定的度量值。 此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。

</dd> <dt>

**FSD \_ Metric4**
</dt> <dd>

指定路由通訊協定特定的度量值。 此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。

</dd> <dt>

**FSD \_ >metric5**
</dt> <dd>

指定路由通訊協定特定的度量值。 此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。

</dd> <dt>

**FSD \_ 旗標**
</dt> <dd>

指定路由是否有效。 路由通訊協定應先清除這些旗標，然後將路由設定為有效或無效。 路由通訊協定應該使用宏 **ClearRouteFlags ()**、 **SetRouteValid ()** 和 **ClearRouteValid ()** 來執行這些作業。 這些宏是在 Rtm 中定義。

</dd> </dl>

## <a name="remarks"></a>備註

路由表管理員會使用 **FSD \_ Priority** 和 **FSD \_ 計量** 成員，來計算特定目的地網路的最佳路由。

**FSD \_ 公制 \[ 1-5 \]** 成員適用于 MIB II 符合規範。 MIB II 代理程式只會顯示這些度量值。 它們不會顯示 **FSD 計量 \_** 度量值。 若要顯示 **FSD \_** 計量，路由通訊協定也應該將值儲存在其中一個 **FSD \_ 公制 \[ 1-5 \]** 成員中。

路由表管理員在計算目的地網路的最佳路由時，不會使用 **FSD \_ 公制 \[ 1-5 \]** 成員中的計量值。 因此，路由通訊協定應確定 FSD 計量 **成員 \_** 具有適當的度量值。

路由通訊協定可以使用 **FSD \_ 旗** 標，將路由標示為無效（如果其他路由通訊協定不應使用路由）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Rtm. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[路由表管理員第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版結構](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> </dl>

 

 





