---
description: 步驟1：建立 Windows Framework
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 步驟1：建立 Windows Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975167"
---
# <a name="step-1-create-the-windows-framework"></a>步驟1：建立 Windows Framework

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

首先，建立 Windows 應用程式的基本架構，包括 WinMain 和視窗程式。 WinMain 函式不會顯示于此處;在訊息迴圈之前呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫，並在訊息迴圈結束後 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。 從下列最基本的視窗程式開始：


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



當您從媒體偵測器取出海報框架時，它會傳回一個緩衝區，其中包含 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，後面接著影像位。 因此，請在視窗程式中定義兩個靜態變數： *pbmi* 會保留 **BITMAPINFOHEADER** 結構的指標，而 *pBuffer* 會保存點陣圖的指標。 應用程式會使用在 *pbmi* 中配置緩衝區 `new` ，因此它必須在終結視窗之前先刪除緩衝區。 *PBuffer* 指標會計算為 *pbmi* 的位移，所以不需要將它刪除。

下一 [步：步驟2：加入功能表命令以抓取海報畫面](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[抓取海報框架](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
