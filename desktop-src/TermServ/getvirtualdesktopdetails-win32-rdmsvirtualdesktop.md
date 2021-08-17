---
title: Win32_RDMSVirtualDesktop 類別的 GetVirtualDesktopDetails 方法
description: 抓取虛擬桌面的其他相關資訊。
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopDetails 方法遠端桌面服務
- GetVirtualDesktopDetails 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetVirtualDesktopDetails 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6ca1b552147623822ae007ca17abf8e4eaebfb149f5e80ac4760719f1ef7168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059486"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Win32 RDMSVirtualDesktop 類別的 GetVirtualDesktopDetails 方法 \_

抓取虛擬桌面的其他相關資訊。

## <a name="syntax"></a>語法


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RAMSizeInMB* \[擴展\]
</dt> <dd>

接收指派給虛擬桌面的 RAM 數量（以位元組為單位）。

</dd> <dt>

*RemoteFXEnabled* \[擴展\]
</dt> <dd>

接收值，指出虛擬桌面上是否已啟用 RemoteFX。 如果已啟用 RemoteFX，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

*OSVersion* \[擴展\]
</dt> <dd>

接收虛擬桌面的作業系統版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





