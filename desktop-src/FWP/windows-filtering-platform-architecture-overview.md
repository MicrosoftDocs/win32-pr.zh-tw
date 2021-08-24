---
title: WFP 架構
description: 本節提供 Windows 篩選平台架構的簡短總覽。
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41989a11ff5412b3185f6987f9588f0309c3fde3ca386c71e4613ab6bc8237f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766600"
---
# <a name="wfp-architecture"></a>WFP 架構

下圖顯示 Windows 篩選平台 (WFP) 的基本架構。

![windows 篩選平臺圖表的基本架構](images/wfp-architecture.png)

## <a name="filter-engine"></a>篩選引擎

篩選引擎包含使用者模式元件和核心模式元件，可共同執行網路資料的所有篩選作業。 篩選引擎包含多個篩選層，這些層級會鬆散對應到作業系統的網路堆疊層。 篩選引擎圖層會根據擁有這些層級的篩選引擎元件，分成使用者模式層和核心模式層。

使用者模式元件會執行 RPC 和 IPsec 篩選。 篩選引擎包含大約10個使用者模式篩選層。

核心模式元件會在 TC/IP 堆疊的網路和傳輸層執行篩選。 此元件也會在 [分類](basic-operation.md) 程式期間呼叫可用的標注函數。 篩選引擎包含大約50的核心模式篩選層。

請參閱 [**篩選圖層識別碼**](management-filtering-layer-identifiers-.md) ，以取得每個篩選引擎層的描述。

## <a name="base-filtering-engine"></a>基礎篩選引擎

基底篩選引擎 (BFE) 是一種使用者模式服務， (bfe.dll 在協調 WFP 元件的 svchost.exe 進程) 中執行。 BFE 執行的主要工作包括從系統新增和移除篩選、儲存篩選器設定，以及強制執行 WFP 設定安全性。 應用程式會透過 [WFP 管理功能](fwp-mgmt-functions.md)與 BFE 進行通訊。

## <a name="callout-drivers"></a>標注驅動程式

注標驅動程式提供額外的篩選功能，方法是將自訂注標函數新增至篩選引擎的一或多個核心模式篩選層。 標注支援深度檢查和封包以及資料流程修改。 在標注驅動程式將其標注函式新增至篩選引擎之後，就可以將指定驅動程式注標函數的篩選加入至篩選程式。 使用者模式管理應用程式或標注驅動程式本身可以新增這類篩選。 在 Windows 開發工具組中提供的核心模式介面，應該只在需要時使用，而不是使用者模式 API 的替代方案。

> [!Note]  
> 如需 callout 驅動程式的詳細資訊，請參閱[Windows 開發工具組](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)的 Windows 篩選平台一節。

 

Windows 篩選平台包含一些內建的 callout 函數，可用於 IPsec 安全資料通訊、可設定狀態的篩選設定，以及隱形模式篩選。 如需內建標注函式的完整清單，請參閱 [**內建的標注識別碼**](built-in-callout-identifiers.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件模型](object-model.md)
</dt> <dt>

[WFP 操作](basic-operation.md)
</dt> <dt>

[Windows篩選平臺標注驅動程式-設計指南](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows篩選平臺標注驅動程式-參考](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 