---
description: 包含 IMFNetCredentialManager 介面的指標。
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: 'MFNETSOURCE_CREDENTIAL_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114000"
---
# <a name="mfnetsource_credential_manager-property"></a>MFNETSOURCE \_ CREDENTIAL \_ MANAGER 屬性

包含 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的指標。 使用這個屬性，將應用程式的 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 執行傳遞至網路來源。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown** 指標

VT \_ 不明

**punkVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ CREDENTIAL \_ MANAGER** 會定義屬性索引鍵的 **GUID** 。  (PID) 的屬性識別碼為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[網路來源驗證](network-source-authentication.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




