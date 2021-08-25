---
description: 衍生所有系統事件追蹤類別的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c083f7a2336a374e8009af2ba8094d57d9826197e16b7577aaf3b00a4c035173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829618"
---
# <a name="msnt_systemtrace-class"></a>MSNT \_ SystemTrace 類別

衍生所有系統事件追蹤類別的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>成員

**MSNT \_ SystemTrace** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSNT \_ SystemTrace** 類別具有這些屬性。

<dl> <dt>

**旗標**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： DefineValues {「事件追蹤旗標進程」、「事件追蹤旗標執行緒」、「事件追蹤旗標映射載入」、「事件追蹤旗標進程計數器」、「事件追蹤旗標」、「事件追蹤旗標」、「事件追蹤旗標中斷」、「事件追蹤旗標」、「事件追蹤旗標 **\_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 磁片 \_ IO」、事件 \_ 追蹤 \_ 旗標磁片檔案 IO」 \_ 、「 \_ \_ 事件 \_ 追蹤旗標 \_ \_ 磁片 \_ IO 初始化」、「事件追蹤旗標 \_ 發送器」、「 \_ \_ \_ 事件 \_ 追蹤旗標 \_ \_ 記憶體 \_ 分頁錯誤」、「事件追蹤旗標 \_ \_ \_ \_ 記憶體 \_ 硬性 \_ 錯誤 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 」、「事件追蹤旗標」、「事件追蹤旗標」、「事件追蹤旗標」事件 \_ 追蹤 \_ 旗標 \_ 分割 \_ IO」、「事件 \_ 追蹤旗標 \_ \_ 驅動程式」、「事件 \_ 追蹤旗標設定檔」、「 \_ \_ 事件 \_ 追蹤旗標檔案 io」、「 \_ \_ \_ 事件 \_ 追蹤 \_ 旗 \_ \_ \_** 標」、「 **0x00000001」、「0x00000002」、「0x00000004」、「0x00000008」、「0x00000010 "、" 0x00000020 "、" 0x00000040 "、" 0x00000080 "、" 0x00000100 "、" 0x00000200 "、" 0x00000400 "、" 0x00000800 "、" 0x00001000 "、" 0x00002000 "、" 0x00004000 "、" 0x00010000** "、" 0x00020000 "、" 0x00100000 "、" 0x00200000 "、" 0x00800000 "、" 0x01000000 "、" 0x02000000 "、" 0x04000000 "}
</dt> </dl>

啟用旗標，指出已啟用的核心提供者。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



 

 




