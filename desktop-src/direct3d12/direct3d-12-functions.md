---
title: " (Direct3D 12 圖形) 的核心功能"
description: 下列函數是在 d3d12 中宣告。
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "106993721"
---
# <a name="core-functions"></a>核心功能

下列函數是在 d3d12 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | 建立代表顯示配接器的裝置。 |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | 還原序列化根簽章，讓您可以判斷 ([**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)) 的版面配置定義。 |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | 產生可透過 [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)傳回還原序列化之資料結構的介面。 |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | 啟用實驗性功能的清單。 |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | 取得 debug 介面。 |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | 序列化可傳遞至 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)的根簽章版本1.0。 |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | 序列化任何可以傳遞給 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)之版本的根簽章。 |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)






