---
title: 'List-View 專案狀態 (CommCtrl) '
description: 專案的狀態值包含專案的狀態、選擇性的覆迭遮罩索引，以及選擇性的狀態影像遮罩索引。
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040272afc16f500806a3d7a90a0b062018d2f4dec8510e4abe57b24cbc75e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958387"
---
# <a name="list-view-item-states"></a>List-View 專案狀態

專案的狀態值包含專案的狀態、選擇性的覆迭遮罩索引，以及選擇性的狀態影像遮罩索引。

專案的狀態決定了其外觀和功能。 狀態可以是零或一或多個下列值：



| 常數                                                                                                                                                                        | 描述                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**LVIS \_ 啟用**</dt> </dl>             | 目前不支援。<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ 剪下**</dt> </dl>                                  | ：項目已標記為進行剪貼作業。<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | ：項目會隨著拖放目標而反白顯示。<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ 焦點**</dt> </dl>                      | 專案具有焦點，因此會以標準焦點矩形括住。 雖然可以選取一個以上的專案，但只有一個專案可以有焦點。<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | 遮罩會取出專案的重迭影像索引。<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS 已 \_ 選取**</dt> </dl>                   | 這個項目已選取。 選取專案的外觀取決於它是否具有焦點，也會顯示用於選取的系統色彩。<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | 遮罩會取出專案的狀態影像索引。<br/>                                                                                                      |



## <a name="remarks"></a>備註

您可以使用 **LVIS \_ OVERLAYMASK** mask 來隔離重迭影像的以一為基礎的索引。 您可以使用 **LVIS \_ STATEIMAGEMASK** mask 來隔離狀態影像的以一為基礎的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





