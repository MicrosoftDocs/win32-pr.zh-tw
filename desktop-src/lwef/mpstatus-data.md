---
title: 'MPSTATUS_DATA 結構 (MpClient .h) '
description: 包含產品元件目前狀態的相關資料。
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA 結構舊版 Windows 環境功能
- PMPSTATUS_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78989b055e6de79c3da733ff8bc498a3fb6717c5dec226db73b80c4e5c9d899c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887908"
---
# <a name="mpstatus_data-structure"></a>MPSTATUS \_ 資料結構

包含產品元件目前狀態的相關資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ComponentID**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 識別碼**](mpcomponent-id.md)**

</dd> <dd>

報告狀態的特定元件識別碼。

</dd> <dt>

**fEnable**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

元件的要求狀態。 回呼資料中的 **hResult** 表示要求成功或失敗。

</dd> <dt>

**ComponentStatus**
</dt> <dd>

根據 **元件** 值的額外狀態資料。

> [!Note]  
> 目前會導致所有適用于 **元件** 的可能值的虛擬結構指標。

 

<dl> <dt>

**p1**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ 為 \_** 簽章時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**又**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ AV \_** 簽章時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p3**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ 即時 \_ 監視** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p4**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ ONACCESS \_ 保護** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p5**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ IOAV \_ 保護** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p6**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ 行為 \_ 監視器** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p7**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ 自動 \_ 掃描** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p8**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ 自動 \_ SIGUPDATE** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**p9**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ IPC** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**Pa**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ NIS** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> <dt>

**鉛**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**

</dd> <dd>

當 **元件**  ==  **MPCOMPONENT \_ ELAM** 時。 請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPCOMPONENT \_ 識別碼**](mpcomponent-id.md)
</dt> <dt>

[**\_ \_ 未使用的 MPSTATUS DATAEX**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





