---
title: 'WINBIO_POLICY_SOURCE 列舉 (Winbio \_ 類型 .h) '
description: 列出針對生物特徵辨識因素偵測詐騙的可能來源原則資訊。
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE 列舉 Windows 生物特徵辨識架構 API
- PWINBIO_POLICY_SOURCE 列舉指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317483"
---
# <a name="winbio_policy_source-enumeration"></a>WINBIO \_ 原則 \_ 來源列舉

列出針對生物特徵辨識因素偵測詐騙的可能來源原則資訊。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO \_ 原則 \_ 不明**
</dt> <dd>

原則的來源不明。

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO \_ 原則 \_ 預設值**
</dt> <dd>

原則是 Windows 生物特徵辨識架構提供的預設原則。

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO \_ 原則 \_ 本機**
</dt> <dd>

個別使用者使用 [ **設定** ] 應用程式為其帳戶設定的原則。 此原則會覆寫預設原則。

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO \_ 原則 \_ 管理員**
</dt> <dd>

IT 系統管理員為企業設定的群組原則。 個別使用者無法覆寫此原則。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





