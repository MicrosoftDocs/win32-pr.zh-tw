---
title: 'WINBIO_EVENT 結構 (Winbio \_ 類型 .h) '
description: 包含引發事件通知時，傳送至回呼常式的狀態資訊。
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EVENT 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3baab16ee7c3f825f317d7aa2c585cb4d8ae7d6d030b6f59a1555b95343015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910541"
---
# <a name="winbio_event-structure"></a>WINBIO \_ 事件結構

**WINBIO \_ 事件** 結構包含引發事件通知時，傳送至回呼常式的狀態資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>成員

<dl> <dt>

**類型**
</dt> <dd>

值，指定所引發之服務提供者事件通知的類型。 目前唯一支援的提供者是指紋感應器。 此感應器支援下列旗標。

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_事件 \_ FP \_ 取消認領** (感應器偵測到應用程式未要求的手指刷，或目前有焦點的視窗。 Windows 生物特徵辨識架構呼叫您的回呼函式，以表示已發生手指刷，但不會嘗試識別指紋。 ) 
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_事件 \_ FP \_ 取消認領 \_ 識別** (感應器偵測到應用程式未要求的手指刷，或目前有焦點的視窗。 Windows 生物特徵辨識架構會嘗試識別指紋，並將該進程的結果傳遞給回呼函式。 ) 
</dt> </dl> </dd> <dt>

**參數**
</dt> <dd> <dl> <dt>

**無人 認領**
</dt> <dd>

針對生物特徵辨識範例抓取傳回的結構。

<dl> <dt>

**UnitId**
</dt> <dd>

產生範例的生物特徵辨識單位。

</dd> <dt>

**RejectDetail**
</dt> <dd>

**ULONG** 值，包含無法捕捉生物特徵辨識範例的其他相關資訊。 如果捕捉成功，這個參數會設定為零。 下列是針對指紋捕捉定義的值：

-   WINBIO \_ FP \_ 太 \_ 高
-   WINBIO \_ FP \_ 太 \_ 低
-   WINBIO \_ FP \_ 太 \_ 左邊
-   WINBIO \_ FP \_ 太 \_ 右邊
-   WINBIO \_ FP \_ 太 \_ FAST
-   WINBIO \_ FP \_ 太 \_ 慢
-   WINBIO \_ FP \_ 品質不佳 \_
-   WINBIO \_ FP \_ 太 \_ 扭曲
-   WINBIO \_ FP \_ 太 \_ 短
-   WINBIO \_ FP \_ 合併 \_ 失敗

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

針對生物特徵辨識捕捉和識別傳回的結構。 識別可判斷範例是否可以與現有的生物特徵辨識範本相關聯。

<dl> <dt>

**UnitId**
</dt> <dd>

產生範例的生物特徵辨識單位。

</dd> <dt>

**身分識別**
</dt> <dd>

[**WINBIO \_ 識別**](winbio-identity.md)結構，其中包含提供生物特徵辨識範例之使用者的 GUID 或 SID。

</dd> <dt>

**SubFactor**
</dt> <dd>

[**WINBIO \_ 生物特徵辨識 \_ 子類型**](winbio-biometric-subtype-constants.md)值，指定與生物特徵辨識範例相關聯的輔助因素。 Windows 生物特徵辨識架構 (WBF) 目前僅支援指紋捕捉，並使用下列常數來表示子類型資訊。

-   WINBIO \_ ANSI \_ 381 \_ POS \_ 不明
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 食指 \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 中間 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 環形 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 小 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 經驗
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 索引 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 中間 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 環形 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 小 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 四 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 四 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ 雙 \_ 拇指

> [!IMPORTANT]
>
> 請勿嘗試驗證針對 *SubFactor* 值提供的值。 Windows 生物特徵辨識服務會先驗證提供的值，再將其傳遞至您的實作為。 如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

**ULONG** 值，包含無法捕捉生物特徵辨識範例的其他相關資訊。 如果捕捉成功，這個參數會設定為零。 下列是針對指紋捕捉定義的值：

-   WINBIO \_ FP \_ 太 \_ 高
-   WINBIO \_ FP \_ 太 \_ 低
-   WINBIO \_ FP \_ 太 \_ 左邊
-   WINBIO \_ FP \_ 太 \_ 右邊
-   WINBIO \_ FP \_ 太 \_ FAST
-   WINBIO \_ FP \_ 太 \_ 慢
-   WINBIO \_ FP \_ 品質不佳 \_
-   WINBIO \_ FP \_ 太 \_ 扭曲
-   WINBIO \_ FP \_ 太 \_ 短
-   WINBIO \_ FP \_ 合併 \_ 失敗

</dd> </dl> </dd> <dt>

**錯誤**
</dt> <dd>

識別要監視之作業成功或失敗的結構。

<dl> <dt>

**ErrorCode**
</dt> <dd>

**HRESULT** 值，包含 \_ 由 Windows 生物特徵辨識架構所執行的計算所產生的 [確定] 或 [錯誤碼]。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)函式以註冊回呼常式，以從 Windows 生物特徵辨識架構接收事件通知。 回呼是您必須為應用程式定義的自訂函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





