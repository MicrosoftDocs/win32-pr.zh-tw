---
description: Delete 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。
ms.assetid: 04d43ac5-b7e6-409f-999a-577232539c15
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8462d097834015883d47ec3da0d70e517a4ead0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966649"
---
# <a name="delete-method-of-the-cim_logicalfile-class"></a>CIM LogicalFile 類別的 Delete 方法 \_

**Delete** 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Delete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。

<dl> <dt>

「成功」
</dt> <dd>

0

成功。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

拒絕存取。

</dd> <dt>

**未指定的失敗**
</dt> <dd>

8

未指定的失敗。

</dd> <dt>

**不正確物件**
</dt> <dd>

9

不正確物件。

</dd> <dt>

**物件已存在**
</dt> <dd>

10

物件已存在。

</dd> <dt>

**檔案系統非 NTFS**
</dt> <dd>

11

檔案系統不是 NTFS。

</dd> <dt>

**平臺非 NT/Windows 2000**
</dt> <dd>

12

平臺不是 Windows。

</dd> <dt>

**磁片磁碟機不相同**
</dt> <dd>

13

磁片磁碟機不相同。

</dd> <dt>

**目錄非空白**
</dt> <dd>

14

目錄未清空。

</dd> <dt>

**共用違規**
</dt> <dd>

15

共用違規。

</dd> <dt>

**不正確開機檔案**
</dt> <dd>

16

不正確啟動檔案。

</dd> <dt>

**未保留許可權**
</dt> <dd>

17

未保留許可權。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

無效的參數。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CIM \_ LogicalFile](delete-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

