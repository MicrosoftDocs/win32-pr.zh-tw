---
title: '隱私範本 (Wininet. h) '
description: 以下是隱私權等級，等同于接受、有條件接受或不接受 cookie 的規則。
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467009"
---
# <a name="privacy-templates"></a>隱私權範本

以下是隱私權等級，等同于接受、有條件接受或不接受 cookie 的規則。 這些層級會對應至 [網際網路選項] 的 [隱私權] 索引標籤上設定的隱私權喜好設定層級。 如需詳細定義，請參閱 [Internet Explorer 6 中的隱私權](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) 。

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**隱私 \_ 範本 \_ 無 \_ COOKIE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



這與封鎖 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 **所有 cookie** 相同。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**隱私 \_ 範本 \_ 高**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



這與 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 [**高**]。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**隱私 \_ 範本 \_ 中度 \_ 高**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



這與 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 [**中 \_ 高**] 相同。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**隱私權 \_ 範本 \_ 媒體**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



這與 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 [**中**] 相同。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**隱私 \_ 範本 \_ 中 \_ 低** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



這與 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 [**低**]。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**隱私 \_ 範本 \_ 低**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



這與 [**網際網路選項**] 的 [隱私權喜好設定] 滑動軸上的 [**接受所有 cookie** ] 相同。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**隱私 \_ 範本 \_ 自訂**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



使用者定義。 請參閱 [如何建立](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) 自訂隱私匯入檔案，以瞭解如何設定自訂隱私權設定。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**隱私權 \_ 範本 \_ ADVANCED**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



使用者定義。 您可以從 [**網際網路選項**] 的 [**隱私權**] 索引標籤，在 [ **advanced 隱私權設定**] 對話方塊中設定 advanced options。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**隱私 \_ 範本 \_ 最大值**
</dt> <dd> <dl> <dt>

隱私 \_ 範本 \_ 低
</dt> <dt>



與 **隱私權 \_ 範本 \_ 低**。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wininet</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

