---
title: 使用 DirectML debug layer
description: DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548397"
---
# <a name="using-the-directml-debug-layer"></a>使用 DirectML debug layer

DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。 Debug 層是個別圖形工具套件的一部分，以隨 [選](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD) 的形式散發。 您必須在系統上安裝圖形工具 FOD，才能使用 debug 圖層。

強烈建議您在使用 DirectML 開發應用程式時啟用 debug 層，因為它可以在 API 使用方式不正確時提供寶貴的資訊。

## <a name="installing-the-directml-debug-layer"></a>安裝 DirectML debug layer

若要視需要安裝選擇性的圖形工具功能 (FOD) 封裝，請從系統管理員 Powershell 提示字元執行下列命令。

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

或者，您也可以從 Windows 10 設定中安裝圖形工具套件。 流覽至 [**設定**  >  **應用**  >  **程式] & 功能**  >  **選擇性功能**  >  **的 [新增功能**> 然後選取 [**圖形工具**]。

## <a name="enabling-the-directml-debug-layer"></a>啟用 DirectML debug layer

安裝圖形工具套件之後，您可以在呼叫 [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice)時提供 [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) ，以啟用 DirectML 的調試層。

> [!IMPORTANT]
> 您必須先啟用 Direct3D 12 debug 層。 然後藉由呼叫 **DMLCreateDevice***來啟用 DirectML* debug layer。

一旦您啟用了 DirectML debug 圖層，任何 DirectML 錯誤或不正確 API 呼叫都會導致以 debug 輸出的形式發出調試資訊。 以下為範例。

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>另請參閱

* [DMLCreateDevice 函式](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [可用的功能-隨選](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [使用以 GPU 為基礎的驗證與 Direct3D 12 Debug Layer](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Direct3D 12 Debug Layer 參考](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
