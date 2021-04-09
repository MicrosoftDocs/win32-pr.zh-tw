---
title: Win32_TSGetIcon 類別的 GetIcon 方法
description: 傳回指定之圖示的內容。
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- GetIcon 方法遠端桌面服務
- GetIcon 方法遠端桌面服務，Win32_TSGetIcon 類別
- Win32_TSGetIcon 類別遠端桌面服務，GetIcon 方法
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934003"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Win32 TSGetIcon 類別的 GetIcon 方法 \_

傳回指定之圖示的內容。

## <a name="syntax"></a>語法


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FilePath* \[在\]
</dt> <dd>

指定檔案的路徑，該檔案包含圖示

</dd> <dt>

*索引* \[在\]
</dt> <dd>

指定檔案中的圖示索引。

</dd> <dt>

*IconContents* \[擴展\]
</dt> <dd>

成功完成時，會包含圖示的內容。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGetIcon**](win32-tsgeticon.md)
</dt> </dl>

 

 





