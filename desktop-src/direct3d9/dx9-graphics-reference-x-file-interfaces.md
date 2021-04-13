---
description: 本節包含用來讀取和寫入 DirectX. x 檔案的 COM 介面參考資訊。 已取代。
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X 檔案介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510145"
---
# <a name="x-file-interfaces"></a>X 檔案介面

本節包含用來讀取和寫入 DirectX. x 檔案的 COM 介面參考資訊。 已取代。

-   [**IDirectXFile**](idirectxfile.md)
-   [**IDirectXFileBinary**](idirectxfilebinary.md)
-   [**IDirectXFileData**](idirectxfiledata.md)
-   [**IDirectXFileDataReference**](idirectxfiledatareference.md)
-   [**IDirectXFileEnumObject**](idirectxfileenumobject.md)
-   [**IDirectXFileObject**](idirectxfileobject.md)
-   [**IDirectXFileSaveObject**](idirectxfilesaveobject.md)

下表說明. x 檔案介面之間的關聯性。



| 介面             | 來自           | 來自 |
|-----------------------|------------------------|--------------|
|                       | IDirectXFile           | IUnknown     |
| IDirectXFileBinary    | IDirectXFileObject     | IUnknown     |
| IDirectXFileData      | IDirectXFileObject     | IUnknown     |
| IDirectXFileReference | IDirectXFileObject     | IUnknown     |
|                       | IDirectXFileSaveObject | IUnknown     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (舊版) 的 X 檔案參考 ](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



