---
description: 您可以藉由執行 IXAPOParameters 介面，將執行時間參數支援新增至 XAPO。 執行時間參數支援可讓 XAPO 根據在執行時間傳遞給它的參數來變更其行為。
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 使用方法：新增 XAPO 的執行階段參數支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf69fcc2570e26f188766a7f908a76d0dfcf3ec190d9fd0d7a1c434b242fdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805538"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>使用方法：新增 XAPO 的執行階段參數支援

您可以藉由執行 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) 介面，將執行時間參數支援新增至 XAPO。 執行時間參數支援可讓 XAPO 根據在執行時間傳遞給它的參數來變更其行為。

1.  遵循 how [to：建立 XAPO](how-to--create-an-xapo.md)中的步驟。
2.  將 XAPO 變更為衍生自 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)。
3.  將 [**CXAPOParametersBase：： BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) 和 [**CXAPOParametersBase：： EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) 方法的呼叫新增至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)的執行。

    > [!Note]  
    > 將這些方法加入至 [IXAPO：:P rocess](how-to--build-a-basic-audio-processing-graph.md) 可讓 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 將其效果參數的複本保存在安全線程狀態中。 在 CXAPOParametersBase 的開頭呼叫 [**CXAPOParametersBase：： BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) （在 [**IXAPO：:P Rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)）和 [**EndProcess：： IXAPO**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) **：:P rocess**。

     

4.  將更多程式碼新增至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 執行，根據 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 方法所儲存的值來變更其行為。

    > [!Note]  
    > 將程式碼加入至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法以使用 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 指定的參數，可讓 XAPO 的行為在整個生命週期中變更。

     

5.  當您建立效果的實例時，請配置三個結構的緩衝區以表示效果的參數，並將其傳遞至 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 的函式。

    > [!Note]  
    > 當您呼叫 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)時， [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)實例會在內部使用這個緩衝區來管理傳遞給它的效果參數。 您必須在呼叫任何 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)、 [**IXAPOParameters：： GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)和 **IXAPOParameters：： SetParameters** 方法之前，將 *pParameterBlocks* 中的所有流程參數區塊初始化為相同的預設值。 此初始化通常會在 [**IXAPO：： Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) 或 [**IXAPO：： LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)中處理。

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAPO 概觀](xapo-overview.md)
</dt> </dl>

 

 
