---
description: 顯示 CXAPOParametersBase 類別的成員。
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: CXAPOParametersBase 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ededac8054229cffa7799ced71653ab19cacf74f705e77163556cc5b60b7655d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770838"
---
# <a name="cxapoparametersbase-members"></a>CXAPOParametersBase 成員

顯示 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 類別的成員。

## <a name="public-constructors"></a>公用建構函式



|    建構函式                                                |     描述                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | 結構 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 物件。 |



 

## <a name="public-methods"></a>公用方法



|        方法                                                                                                                      |     描述                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                          | 遞增 XAPO 物件的參考計數。<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | 傳回目前的進程參數。 <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                            | 傳回產生指定之輸出框架數目所需的輸入框架數目。<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                          | 傳回產生指定之輸入框架數目所需的輸出框架數目。<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | 通知 [**CXAPOPARAMETERSBASE**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) XAPO 已完成存取目前的進程參數。 <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (繼承自 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters))  | 取得特定效果的參數。 <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))        | 傳回 XAPO 的註冊屬性。<br/>                                                                                                       |
|  (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) 的 [**初始化**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize)                                     | 執行任何效果特定的初始化。<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))              | 查詢指定的輸出格式是否支援特定的輸入格式。<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))            | 查詢指定的輸入格式是否支援特定的輸出格式。<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                              | 將會提供 XAPO 串流格式 [**流程**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 的通知。<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | 由 [**IXAPOParameters：： SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 呼叫，以允許使用者定義的參數驗證。 <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | 指出自上一次處理之後是否已呼叫 [**IXAPOParameters：： SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 。 <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                          | 如果 XAPO 支援要求的介面指標，則予以抓取。<br/>                                                                                    |
| [**版本**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                        | 遞減 XAPO 物件的參考計數，並在參考計數降至零時刪除物件。<br/>                                             |
| [**重設**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                                | 將物件傳回至呼叫 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 之後的狀態。<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (繼承自 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters))  | 設定效果特定的參數。<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (繼承自 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                          | 相反地，LockForProcess：在 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 期間配置的變數應該在此方法中解除配置。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CXAPOParametersBase 類別**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
