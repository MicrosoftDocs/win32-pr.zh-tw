---
description: LINEOPENOPTION \_ 常數列出可用來開啟行的選項。
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: 'LINEOPENOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997727"
---
# <a name="lineopenoption_-constants"></a>LINEOPENOPTION \_ 常數

**LINEOPENOPTION \_ 常數** 列出可用來開啟行的選項。

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION \_ PROXY**
</dt> <dd> <dl> <dt>



應用程式願意處理來自已開啟行之其他應用程式的要求。


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



只有在行裝置上所指定的位址出現在 *lpCallParams* 參數所指向之 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwAddressID** 成員中指定的位址時，應用程式才會收到新呼叫的通知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如需這些選項的詳細資訊，請參閱 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




