---
description: 設定出現在 wizard 標頭中的標題和副標題。 一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。
title: 'WebWizardHost. SetHeaderText 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841829"
---
# <a name="webwizardhostsetheadertext-method"></a>WebWizardHost. SetHeaderText 方法

設定出現在 wizard 標頭中的標題和副標題。 一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。

## <a name="syntax"></a>語法


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrHeaderTitle* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含標題的字串。

</dd> <dt>

*bstrHeaderSubtitle* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含子標題的字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 
