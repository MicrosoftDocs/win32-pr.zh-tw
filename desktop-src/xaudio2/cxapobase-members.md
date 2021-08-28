---
description: 顯示 CXAPOBase 類別的成員。
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: CXAPOBase 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e76e1846b5dd9c28bec4f5cfe8e0168f5afbca012459b5860c4a5e23c610f6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962737"
---
# <a name="cxapobase-members"></a>CXAPOBase 成員

顯示 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 類別的成員。

## <a name="public-constructors"></a>公用建構函式



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | 結構 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 物件。 |



 

## <a name="public-methods"></a>公用方法



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                    | 遞增 XAPO 物件的參考計數。<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                      | 傳回產生指定之輸出框架數目所需的輸入框架數目。<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                    | 傳回產生指定之輸入框架數目所需的輸出框架數目。<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))  | 傳回 XAPO 的註冊屬性。<br/>                                                                                                       |
|  (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) 的 [**初始化**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize)                               | 執行任何效果特定的初始化。<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))        | 查詢指定的輸出格式是否支援特定的輸入格式。<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))      | 查詢指定的輸入格式是否支援特定的輸出格式。<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                        | 將會提供 XAPO 串流格式 [**流程**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 的通知。<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                    | 如果 XAPO 支援要求的介面指標，則予以抓取。<br/>                                                                                    |
| [**版本**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                  | 遞減 XAPO 物件的參考計數，並在參考計數降至零時刪除物件。<br/>                                             |
| [**重設**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                          | 將物件傳回至呼叫 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 之後的狀態。<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                    | 相反地，LockForProcess：在 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 期間配置的變數應該在此方法中解除配置。<br/> |



 

## <a name="protected-methods"></a>保護方法



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | 傳回 [**XAPO \_ 註冊 \_ 屬性**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)S 結構的指標，其中包含 XAPO 建立時所使用的註冊屬性。<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | 檢查 XAPO 是否已鎖定。<br/>                                                                                                                                                |
| 長 m \_ lReferenceCount<br/>                                                       | XAPO 物件的 COM 參考計數。<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | 由 IXAPO 所呼叫：當 XAPO 停用以供處理時， [**:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 執行。<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | 確認音訊格式是否落在支援的預設範圍內。<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | 根據 XAPO 屬性旗標，確認是否支援輸入和輸出格式配對設定。<br/>                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CXAPOBase 類別**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
