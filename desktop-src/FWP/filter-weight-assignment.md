---
title: 篩選器加權指派
description: Windows 篩選平台 (WFP) 中的每個篩選都有相關聯的權數，可在篩選仲裁期間使用。
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746868"
---
# <a name="filter-weight-assignment"></a>篩選器加權指派

Windows 篩選平台 (WFP) 中的每個篩選都有相關聯的權數，可在[篩選仲裁](filter-arbitration.md)期間使用。

基底篩選引擎 (BFE) 所使用的篩選權數屬於類型的 [**.Fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。 呼叫端在新增篩選時有三個選項。

-   將權數設定為 [**.Fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。 BFE 使用提供的權數。
-   將權數設為 [**\_ 空**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)的。 BFE 會自動產生範圍 \[ 0、2⁶⁰) 的加權。
-   將權數設定為範圍0、15中的 [**.Fwp \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) \[ \] 。 BFE 使用提供的權數作為權數範圍識別碼。

    BFE 會自動產生低序位60位 (完全如同權數已設定為 [**.Fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) ，然後使用提供的值來設定4個高序位位。 這可讓呼叫者手動將權數空間分割成16個範圍，同時仍然在範圍內使用自動加權。

> [!Note]  
> 當兩個以上的標注都在相同的子層級註冊時，當相同的加權指派給篩選器時，可能會發生問題。 使用 [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)來建立自己的子層，可避免這個問題。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**篩選權數識別碼**](filter-weight-identifiers.md)
</dt> </dl>

 

 




