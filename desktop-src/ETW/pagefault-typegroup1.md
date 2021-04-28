---
description: PageFault_TypeGroup1 類別-這個類別是分頁錯誤事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106406"
---
# <a name="pagefault_typegroup1-class"></a>PageFault \_ TypeGroup1 類別

此類別是分頁錯誤事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>成員

**PageFault \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**PageFault \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

正在執行的目前指令指標。

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

造成分頁錯誤之頁面的虛擬位址。

</dd> </dl>

## <a name="remarks"></a>備註

如果找不到在記憶體快取中找出的頁面，而且必須從記憶體中的其他位置取出 (軟錯誤) 或從磁片 (硬性錯誤) ，就會發生分頁錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




