---
description: 這個類別是取樣設定檔事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: SampledProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973649"
---
# <a name="sampledprofile-class"></a>SampledProfile 類別

這個類別是取樣設定檔事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>成員

**SampledProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SampledProfile** 類別具有這些屬性。

<dl> <dt>

**Count**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

未使用。

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

取樣處理器時正在執行之映射的位址。

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

取樣處理器時正在執行之執行緒的執行緒識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

這些事件會提供取樣的執行設定檔。 事件會記錄在處理器上執行的專案。 您可以使用影像事件來識別包含該指令的二進位模組。 然後，您可以使用這項資訊，在追蹤期間產生執行設定檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




