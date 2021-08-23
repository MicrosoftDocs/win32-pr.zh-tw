---
title: 'MCI_VCR_STATUS_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ status \_ PARMS 結構包含適用于 \_ video/磁帶燒錄機的 mci status 命令參數。
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8569a278f697ed816085c4fc8f313502d2994215519fb2452f82e63ce31a80cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783918"
---
# <a name="mci_vcr_status_parms-structure"></a>MCI \_ VCR \_ 狀態 \_ PARMS 結構

**Mci \_ VCR \_ status \_ PARMS** 結構包含適用于 video/磁帶燒錄機的 [**mci \_ status**](mci-status.md)命令參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwReturn**
</dt> <dd>

[**MCI \_ STATUS**](mci-status.md)命令所傳回的值。 傳回值會根據命令的查詢而有所不同。 如需詳細資訊，請參閱 [**MCI \_ STATUS**](mci-status-parms.md) 命令的描述。

</dd> <dt>

**dwItem**
</dt> <dd>

要求的資訊類型。

</dd> <dt>

**dwTrack**
</dt> <dd>

將在下次錄製期間儲存資訊的音訊或影片播放軌。 當 [**MCI \_ STATUS**](mci-status-parms.md) 命令查詢影片或音訊錄製狀態時，此成員會用來傳回信息。

</dd> <dt>

**dwNumber**
</dt> <dd>

與目前通道相關聯的邏輯調諧器。 當 [**MCI \_ STATUS**](mci-status.md) 命令查詢目前的通道號碼時，此成員會用來傳回信息。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vcr</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 狀態**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

