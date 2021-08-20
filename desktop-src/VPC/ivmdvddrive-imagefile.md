---
title: 'IVMDVDDrive ImageFile 屬性 (VPCCOMInterfaces .h) '
description: 抓取此裝置之影像檔案的完整路徑。
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- 虛擬 PC 的 ImageFile 屬性
- ImageFile 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，ImageFile 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275826aaea8dcb4f40427f2448a5edc86a992aefa4dc81648703a5f0a2948604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123753"
---
# <a name="ivmdvddriveimagefile-property"></a>IVMDVDDrive：： ImageFile 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此裝置之影像檔案的完整路徑。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>屬性值

影像檔案的完整路徑。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                            | 意義                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                               | 作業成功。<br/>                                  |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                 | 參數為 **Null**。<br/>                                     |
| <dl> <dt>E \_FAIL</dt> <dt>0x80004005</dt> </dl>                    | 已發生未預期的錯誤。<br/>                              |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>         | 找不到虛擬機器。<br/>                        |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl>      | 此磁片磁碟機的匯流排位置無效。<br/>                  |
| <dl> <dt>VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型</dt> <dt>0xA00400728</dt> </dl> | 由此 DVD 光碟機所捕捉的媒體不是 ISO 影像檔案。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>         | 已發生未預期的錯誤。<br/>                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

