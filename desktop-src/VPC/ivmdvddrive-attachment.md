---
title: 'IVMDVDDrive 附件屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中連接至 DVD 光碟機的媒體類型。
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- 附加屬性虛擬電腦
- 附加屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，附件屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843952"
---
# <a name="ivmdvddriveattachment-property"></a>IVMDVDDrive：：附件屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬機器中連接至 DVD 光碟機的媒體類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a>屬性值

附加的媒體類型。 如需值的清單，請參閱 [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md)。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                       | 意義                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                          | 作業成功。<br/>               |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>            | 參數為 **Null**。<br/>                  |
| <dl> <dt>E \_FAIL</dt> <dt>0x80004005</dt> </dl>               | 已發生未預期的錯誤。<br/>           |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>    | 找不到虛擬機器。<br/>     |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl> | 此磁片磁碟機的匯流排位置無效。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>    | 已發生未預期的錯誤。<br/>           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

