---
description: 這些旗標會指定媒體定位器的行為。
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: '檔案名驗證旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985564"
---
# <a name="file-name-validation-flags"></a>檔案名驗證旗標

\[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

這些旗標會指定媒體定位器的行為。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_VALIDATEF \_ 檢查**</dt> <dt>0x01</dt> </dl>                   | 檢查檔案名的有效性。 您必須設定這個旗標以驗證檔案名。 如果不是，則其他旗標沒有任何作用。<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_VALIDATEF \_ POPUP**</dt> <dt>0x02</dt> </dl>                   | 如果找不到檔案，則會顯示使用者的 [開啟檔案] 對話方塊。<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | 如果找不到檔案，請使用檔案的名稱和位置來短暫顯示訊息方塊。 此旗標大多適用于測試用途;訊息方塊可能不適合零售產品。<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_VALIDATEF \_ REPLACE**</dt> <dt>0x08</dt> </dl>             | 如果找不到檔案，請更新來源物件的名稱。  (僅適用于 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md) 方法。 ) <br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | 一律使用本機檔案，即使網路上有檔案版本也一樣。<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_VALIDATEF \_ NOFIND**</dt> <dt>0x20</dt> </dl>                | 請勿搜尋遺失的檔案。 如果您設定 SFN \_ VALIDATEF 檢查旗標，仍會驗證檔案名 \_ 。<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | 略過靜音來源物件。  (僅適用于 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md) 方法。 ) <br/>                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




