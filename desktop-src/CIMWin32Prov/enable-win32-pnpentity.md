---
description: 啟用此隨插即用裝置。
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Enable Win32_PnPEntity 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971953"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a>Enable Win32 \_ PnPEntity 類別的方法

啟用此隨插即用裝置。

## <a name="syntax"></a>語法


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rebootNeeded* \[擴展\]
</dt> <dd>

是否需要重新開機。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 




