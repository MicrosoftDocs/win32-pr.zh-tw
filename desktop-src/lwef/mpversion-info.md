---
title: 'MPVERSION_INFO 結構 (MpClient .h) '
description: 惡意程式碼防護管理員元件的版本資訊。
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO 結構舊版 Windows 環境功能
- PMPVERSION_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608698"
---
# <a name="mpversion_info-structure"></a>MPVERSION \_ 資訊結構

惡意程式碼防護管理員元件的版本資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**產品**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

產品版本。

</dd> <dt>

**服務**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

服務元件版本。

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

檔案系統篩選元件版本。

</dd> <dt>

**引擎**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

引擎元件版本。

</dd> <dt>

**ASSignature**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

防毒軟體簽章元件版本。

</dd> <dt>

**AVSignature**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

防毒軟體特徵碼元件版本。

</dd> <dt>

**NISEngine**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

NIS 引擎版本。

</dd> <dt>

**NISSignature**
</dt> <dd>

類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**

</dd> <dd>

NIS 簽名碼元件版本。

</dd> <dt>

**已保留**
</dt> <dd>

類型： **[**MPCOMPONENT \_**](mpcomponent-version.md) \[ 第4版\]**

</dd> <dd>

保留的欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPCOMPONENT \_ 版本**](mpcomponent-version.md)
</dt> </dl>

 

 





