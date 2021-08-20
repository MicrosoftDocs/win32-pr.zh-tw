---
description: 用來報告狀態或錯誤資訊，以回應 SCSI 要求感知命令。
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: 'SENSE_DATA 結構 (Scsi-3) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: 2f6b3bd9fd4353e396bc7fe4ff7273e598704d1348062fec1c2f64aed9380686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075951"
---
# <a name="sense_data-structure"></a>意義 \_ 資料結構

用來報告狀態或錯誤資訊，以回應 SCSI **要求感知** 命令。

## <a name="syntax"></a>語法


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ErrorCode**
</dt> <dd>

報表類型。



| 值                                                                           | 意義                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | 目前的錯誤。<br/>  |
| <dl> <dt>0x71</dt> </dl> | 延遲的錯誤。<br/> |



 

</dd> <dt>

**有效**
</dt> <dd>

如果 **資訊** 欄位定義于標準中，則為1。否則， **資訊** 欄位是廠商專屬的，而且不是由標準所定義。

</dd> <dt>

**SegmentNumber**
</dt> <dd>

已過時。

</dd> <dt>

**SenseKey**
</dt> <dd>

指出錯誤的類別。

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**沒有意義** (0x0) 
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**復原的錯誤** (0x1) 
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (0x2) 
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**中度錯誤** (0x3) 
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**硬體錯誤** (0x4) 
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>不 **合法的要求** (0x5) 
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span> (0x6) 的 **單元注意**
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**資料保護** (0x7) 
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span> (0x9) 的 **固件錯誤**
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**中止的命令** (0xB) 
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**等於** (0xC) 
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span> (0xD) 的 **磁片區溢** 位
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE) 
</dt> </dl> </dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1，如果要求的邏輯區塊長度不符合媒體上資料的邏輯區塊長度。

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1，如果連續存取裝置已到達媒體的結尾，或印表機已缺紙。

</dd> <dt>

**尚未調准**
</dt> <dd>

如果目前的命令已到達標記或 setmark，則為1。 僅適用于順序存取裝置。

</dd> <dt>

**資訊**
</dt> <dd>

裝置類型或命令特有的資料。

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

結構其餘部分的長度（以位元組為單位）。 總長度減去7。

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

命令特有的資料。 值是在適當的命令標準中定義。

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

描述 **SenseKey** 欄位中所報告之錯誤的裝置特定程式碼。

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

可以包含 **AdditionalSenseCode** 欄位的其他詳細資料。

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

與此意義資料相關聯之元件的 Vender 特定資訊。

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

意義重要的特定資訊的內容和格式是由 **SenseKey** 欄位的值所決定。

</dd> </dl>

## <a name="remarks"></a>備註

如需有關意義資料格式的詳細資訊，請參閱 [SCSI 要求感知命令](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Scsi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[iSCSI 目標傳遞](/powershell/module/iscsi)
</dt> <dt>

[SCSI \_ \_ 通過 \_ DIRECT](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




