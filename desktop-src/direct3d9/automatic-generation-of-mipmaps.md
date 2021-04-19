---
description: 您現在可以自動建立一系列紋理的 mipmap，每個都篩選成不同的解析度。
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: '自動產生 Mipmap (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972141"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>自動產生 Mipmap (Direct3D 9) 

您現在可以自動建立一系列紋理的 mipmap，每個都篩選成不同的解析度。 Mipmap 通常用來在轉譯時提供不同層級的詳細資料。 在紋理建立時間中自動產生 Mipmap 可以利用硬體篩選，因為 Mipmap 位於視訊記憶體中。

若要自動產生 mipmap，請在呼叫 [**CreateTexture**](/windows/desktop/api)之前，先設定新的使用方式 [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) 。 從這個點開始的子層級，對應用程式而言是完全透明的。 應用程式只能存取最上層材質層級;材質子層無法存取，因為它們只會在驅動程式需要時才會建立。 如果子層代可能需要很長的時間，請使用 [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) 提示驅動程式，它應該會在應用程式的適當時間產生子層級。

## <a name="mipmap-filtering"></a>Mipmap 篩選

[**SetAutoGenFilterType**](/windows/desktop/api) 會在自動產生期間控制篩選品質。 變更篩選類型會 dirties mipmap 子層級，並使其重新產生。 使用 [**GetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) 取得目前的篩選類型。 預設篩選類型為 D3DTEXF \_ 線性。 如果驅動程式不支援線性篩選，則篩選器類型會設定為 D3DTEXF \_ 點。

如果紋理不是使用 [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) 建立的，而且沒有傳回任何失敗，這些方法就不會有任何作用。 除了 D3DTEXF NONE 之外，驅動程式支援一般材質篩選的所有篩選類型都支援自動產生 \_ 。 針對每個資源類型，驅動程式應該支援對應材質、CubeTexture 和 volumetexture 篩選器中所報告的所有篩選器類型。

若要檢查支援的篩選器類型，請檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 TextureFilterCaps 和/或 CubeTextureFilterCaps 成員支援哪些 caps。

## <a name="mipmap-support"></a>Mipmap 支援

[D3DUSAGE \_AUTOGENMIPMAP](d3dusage.md) 只是一個提示，在材質建立期間或在呼叫 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 時，不會造成任何設備磁碟機介面 (DDI) 類型的錯誤。

當來源是自動產生的 mipmap，但目的地不是時，呼叫 [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 是不合法的。 來源可以是非自動產生的 mipmap，而且目的地可以是自動產生的 mipmap。 在此情況下，只會更新最上層的比對層級。 系統會忽略所有其他來源子層級。 同樣地，當來源和目的地都自動產生時，只會更新最上層的比對層級。 系統會忽略來源中的子層級，並重新產生目的地子級別。

若要檢查是否支援自動產生 mipmap，請檢查是否已設定 [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) 。 如果是，請使用 [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md)來呼叫 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 。 如果傳回值為「D3D」 \_ ，則 mipmap 保證會自動產生。 如果傳回值是 D3DOK \_ NOAUTOGEN，這表示建立呼叫會成功，但不會產生任何 mipmap。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
