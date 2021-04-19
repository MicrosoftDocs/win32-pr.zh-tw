---
description: LINEFEATURE \_ 常數列出可以使用此 API 在行上叫用的作業。
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: 'LINEFEATURE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995098"
---
# <a name="linefeature_-constants"></a>LINEFEATURE \_ 常數

**LINEFEATURE \_ 常數** 列出可以使用此 API 在行上叫用的作業。

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



裝置特定的作業可以使用於這一行。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**
</dt> <dd> <dl> <dt>



裝置特定功能可以在這一行上使用。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**\_向前 LINEFEATURE**
</dt> <dd> <dl> <dt>



所有位址的轉送都可以使用於這一行。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式 (有空白的目的地位址) 可用來開啟行上所有位址的「請勿打擾」功能。 \_也會設定 LINEFEATURE 轉寄。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式可以用來將該行上所有位址的呼叫轉送到其他數位。 \_也會設定 LINEFEATURE 轉寄。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



您可以使用未指定的位址，將外寄呼叫放在這一行。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**
</dt> <dd> <dl> <dt>



您可以線上路裝置上叫用 [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) 函式。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



您可以在這一行設定媒體控制項。


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



您可以設定這一行的終端模式。

> [!Note]  
> 如果在 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)的 **dwLineFeatures** 成員中未設定新的已修改 "FORWARD" 位 \_ ，但已設定 LINEFEATURE 轉寄位，則任何轉寄模式都可以運作，而服務提供者只會指定哪一個。

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

LINEFEATURE \_ 常數用於 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)) 所傳回的 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (。 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) 報表，適用于給定的行，在行處於目前狀態時，可以實際叫用的線條特徵。 應用程式會在行狀態變更之後動態進行這項判斷，通常是由一行上的位址或呼叫相關的活動所造成。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




