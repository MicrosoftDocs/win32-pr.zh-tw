---
description: 預設會允許 Direct3D 系統寫入深度緩衝區。 大部分的應用程式會讓寫入深度緩衝區保持啟用狀態，但您可以藉由不允許 Direct3D 系統寫入深度緩衝區來達成某些特殊效果。
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: '變更深度緩衝區寫入存取 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973772"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>變更深度緩衝區寫入存取 (Direct3D 9) 

預設會允許 Direct3D 系統寫入深度緩衝區。 大部分的應用程式會讓寫入深度緩衝區保持啟用狀態，但您可以藉由不允許 Direct3D 系統寫入深度緩衝區來達成某些特殊效果。

您可以在 c + + 中停用深度緩衝區寫入，方法是呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，並將 State 參數設定為 D3DRS \_ ZWRITEENABLE，並將 Value 參數設定為0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
