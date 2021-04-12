---
description: 在繼承應用程式中使用下列程式載入 x.x 檔案。
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: '載入 X 檔案 (舊版)  (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509953"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>載入 X 檔案 (舊版)  (Direct3D 9) 

在繼承應用程式中使用下列程式載入 x.x 檔案。

1.  您可以使用 [**DirectXFileCreate**](directxfilecreate.md) 函數來建立 [**IDirectXFile**](idirectxfile.md) 物件。
2.  如果範本存在於您將載入的 DirectX 檔案中，請使用 [**IDirectXFile：： RegisterTemplates**](idirectxfile--registertemplates.md) 方法來註冊這些範本。
3.  使用 [**IDirectXFile：： CreateEnumObject**](idirectxfile--createenumobject.md) 方法來建立 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 列舉值物件。
4.  迴圈流覽檔案中的物件。 針對每個物件，執行下列步驟。
    1.  使用 [**IDirectXFileEnumObject：： GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) 方法來取出每個 [**IDirectXFileData**](idirectxfiledata.md) 物件。
    2.  您可以使用 [**IDirectXFileData：： GetType**](idirectxfiledata--gettype.md) 方法來取出資料的型別。
    3.  使用 [**IDirectXFileData：：：：**](idirectxfiledata--getdata.md) 的方法載入資料。
    4.  如果物件具有選擇性成員，請藉由呼叫 [**IDirectXFileData：： GetNextObject**](idirectxfiledata--getnextobject.md) 方法來取出選擇性成員。
    5.  釋放 [**IDirectXFileData**](idirectxfiledata.md) 物件。
5.  釋放 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 物件。
6.  釋放 [**IDirectXFile**](idirectxfile.md) 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[X 檔案 (舊版) ](x-files--legacy-.md)
</dt> </dl>

 

 



