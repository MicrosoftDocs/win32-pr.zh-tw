---
description: 更新用戶端的 wizard 框架中的 [上一頁]、[下一頁] 和 [完成] 按鈕。
title: 'WebWizardHost. SetWizardButtons 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842619"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>WebWizardHost. SetWizardButtons 方法

更新用戶端的 wizard 框架中的 [ **上一頁**]、 **[下一頁**] 和 **[完成]** 按鈕。

## <a name="syntax"></a>語法


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vbEnableBack* \[在\]
</dt> <dd>

類型： **布林值**

啟用 [ **上一頁** ] 按鈕。

</dd> <dt>

*vbEnableNext* \[在\]
</dt> <dd>

類型： **布林值**

啟用 [下一步] 按鈕。

</dd> <dt>

*vbLastPage* \[在\]
</dt> <dd>

類型： **布林值**

啟用 [ **完成]** 按鈕。 指出這是最後一個伺服器端頁面。

</dd> </dl>

## <a name="remarks"></a>備註

請務必在 OnBack () 和 OnNext () 的每個伺服器端頁面中，執行處理常式函式，這會對應至 wizard 按鈕 **回來** 和 **下一步**。 OnBack () 和 OnNext () 函數會回應 **SetWizardButtons**。 在適當的時間，OnNext () 函式會呼叫 **SetWizardButtons** 和 *vbLastPage* = **true**，以啟用 **[完成]** 按鈕。 OnNext () 也會在使用者按一下 [**完成]** 按鈕時呼叫 [**FinalNext**](iwebwizardhost-finalnext.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 




