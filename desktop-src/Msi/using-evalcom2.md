---
description: Evalcom2.dll 可以用來利用內部一致性評估工具來執行安裝套件和合併模組的驗證作業。
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: 使用 Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527120"
---
# <a name="using-evalcom2"></a>使用 Evalcom2

Evalcom2.dll 可以用來利用 [內部一致性評估](internal-consistency-evaluators-ices.md)工具來執行安裝套件和合併模組的驗證作業。 主要物件會執行 C/c + + 程式的介面。

主要物件也會針對 C/c + + 程式執行 [Evalcom2 介面](evalcom2-interfaces.md) 。 從 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 取得介面所需的 CLSID 為 {6E5E1910-8053-4660-B795-6B612E29BC58}。 REFIID 是 {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}。

您可以使用下列程式來執行驗證作業。

**若要執行驗證作業**

1.  使用 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize)初始化呼叫執行緒上的 COM。
2.  使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)取得 [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate)介面的指標。
3.  使用 [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) 方法開啟安裝封裝或合併模組。
4.  使用 [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) 方法開啟評估檔案。
5.  使用 [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) 方法來設定顯示回撥函式。
6.  使用 [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) 方法設定狀態回呼函數。
7.  使用 [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) 方法來執行驗證。
8.  使用 [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) 方法來關閉 .cub 檔。
9.  使用 [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) 方法來關閉資料庫。
10. 釋放 [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) 介面。
11. 使用 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)將 COM 解除初始化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Evalcom2 介面](evalcom2-interfaces.md)
</dt> <dt>

[驗證自動化](validation-automation.md)
</dt> <dt>

[驗證回呼函數](validation-callback-functions.md)
</dt> </dl>

 

 
