---
title: 'IVMFloppyDrive ImageFile 屬性 (VPCCOMInterfaces .h) '
description: 抓取連接軟碟磁碟機之影像檔案的完整路徑。
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- 虛擬 PC 的 ImageFile 屬性
- ImageFile 屬性 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，ImageFile 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44c76498d192954dde50e3f997fe91ce405344fc2048697ce996723aa0e6d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595118"
---
# <a name="ivmfloppydriveimagefile-property"></a>IVMFloppyDrive：： ImageFile 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取連接軟碟磁碟機之影像檔案的完整路徑。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a>屬性值

影像檔案的完整路徑。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                               |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                                                  |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 此虛擬機器的設定無效或找不到。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

