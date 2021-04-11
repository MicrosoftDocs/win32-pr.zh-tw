---
description: 在繼承應用程式中使用下列程式，將. x 檔案範本和資料儲存至 x.x 檔案。
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: '儲存至 X 檔案 (舊版)  (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317655"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>儲存至 X 檔案 (舊版)  (Direct3D 9) 

在繼承應用程式中使用下列程式，將. x 檔案範本和資料儲存至 x.x 檔案。

1.  您可以使用 [**DirectXFileCreate**](directxfilecreate.md) 函數來建立 [**IDirectXFile**](idirectxfile.md) 物件。
2.  使用 [**IDirectXFile：： RegisterTemplates**](idirectxfile--registertemplates.md) 方法，通知 DirectX 檔案系統有關您將使用的任何範本。
3.  使用 [**IDirectXFile：： CreateSaveObject**](idirectxfile--createsaveobject.md) 方法來建立 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 物件。
4.  如有需要，請使用 [**IDirectXFileSaveObject：： SaveTemplates**](idirectxfilesaveobject--savetemplates.md) 方法來儲存範本。
5.  迴圈處理要儲存的物件。 針對每個最上層物件，執行下列步驟。
    -   使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 [**IDirectXFileData**](idirectxfiledata.md) 物件，做為檔案中的最上層物件。 如果最上層資料物件有選擇性的子物件，請使用下一個步驟中的適當方法，將它們新增至物件。
    -   如果物件的範本允許，每個 [**IDirectXFileData**](idirectxfiledata.md) 物件都可以有選擇性的子物件。 子物件可以是下列三種類型的物件之一： **IDirectXFileData**、 [**IDirectXFileDataReference**](idirectxfiledatareference.md)或 [**IDirectXFileBinary**](idirectxfilebinary.md)。 迴圈處理您需要儲存的物件，將每個選擇性的子成員以適當的類型加入至物件清單，如下列步驟所示。 然後，如果物件類型是 Data，請呼叫 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 **IDirectXFileData** 物件，然後呼叫 [**IDirectXFileData：： AddDataObject**](idirectxfiledata--adddataobject.md) 方法，將它新增為物件的子系。 如果物件類型是資料參考，請呼叫 [**IDirectXFileData：： AddDataReference**](idirectxfiledata--adddatareference.md) 方法，以建立資料參考物件，並將其加入為物件的子系。 或者，如果物件類型是 Binary，請呼叫 [**IDirectXFileData：： AddBinaryObject**](idirectxfiledata--addbinaryobject.md) 方法，以建立二進位物件，並將其新增為物件的子系。
    -   呼叫 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md) 方法，以儲存資料物件和其子系。
    -   釋放 [**IDirectXFileData**](idirectxfiledata.md) 物件。
6.  釋放 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 物件。
7.  釋放 [**IDirectXFile**](idirectxfile.md) 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[X 檔案 (舊版) ](x-files--legacy-.md)
</dt> </dl>

 

 



