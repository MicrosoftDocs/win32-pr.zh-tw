---
title: IMsRdpClientShell RdpFileContents 屬性
description: 指定或抓取從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動的遠端桌面通訊協定 (RDP) 檔案內容。
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- RdpFileContents 屬性遠端桌面服務
- RdpFileContents 屬性遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，RdpFileContents 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967744"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>IMsRdpClientShell：： RdpFileContents 屬性

指定或抓取從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動的遠端桌面通訊協定 (RDP) 檔案內容。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>屬性值

指定要從 web 入口網站啟動的 RDP 檔案內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





