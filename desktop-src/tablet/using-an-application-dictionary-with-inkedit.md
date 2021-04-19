---
description: 若要建立應用程式字典，必須設定 RecognizerCoNtext 物件的單詞表屬性。
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: 使用應用程式字典搭配 InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc919fc071f249611d42b8decb6ce4fb0b0f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973257"
---
# <a name="using-an-application-dictionary-with-inkedit"></a>使用應用程式字典搭配 InkEdit

若要建立應用程式字典，必須設定 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性。 [InkEdit](inkedit-control-reference.md)控制項不會公開 **RecognizerCoNtext** 物件，因此不可能直接設定 InkEdit 控制項 **RecognizerCoNtext** 物件的 **單詞表** 屬性。

若要搭配使用應用程式字典與 [InkEdit](inkedit-control-reference.md) 控制項，您必須將筆劃從 InkEdit 控制項移至新的 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件，並將 [ [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) ] 屬性設定為包含應用程式字典的 [**單詞表**](inkwordlist-class.md) 、儲存此 **RecognizerCoNtext** 物件的結果，然後將結果傳回 InkEdit 控制項。

## <a name="example"></a>範例

下列 C \# 程式碼顯示這項技術的範例。


```C++
private RecognizerContext rc;
private WordList wl;
private int wlSelStart;
private int wlSelLen;
private bool isRecoPending = false;

private void Form1_Load(object sender, EventArgs e)
{
  //event handlers must be attached for dictionary to work.
  inkEdit1.Recognition += new Microsoft.Ink.InkEditRecognitionEventHandler(inkEdit1_Recognition);
  inkEdit1.TextChanged += new EventHandler(inkEdit1_TextChanged);

  //create a WordList that contains the application dictionary
  wl = new WordList();
  //...
  //Add dictionary terms to the WordList
  //...

  // create a RecognizerContext for the WordList
  rc = inkEdit1.Recognizer.CreateRecognizerContext();
  rc.Factoid = Factoid.WordList;

  //set the RecognizerContext WordList to the newly created WordList
  rc.WordList = wl;

  //create a delegate for the new RecognizerContext
  rc.RecognitionWithAlternates += new

  RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition);
}

void inkEdit1_TextChanged(object sender, EventArgs e)
{
  if (isRecoPending)
  {
    isRecoPending = false;
    rc.BackgroundRecognizeWithAlternates();
  }
}

private void inkEdit1_Recognition(object sender,
Microsoft.Ink.InkEditRecognitionEventArgs e)
{
  //store the start of the selection in wlSelStart
  wlSelStart = inkEdit1.SelectionStart;

  //store the length of the selection in wlSelLen
  wlSelLen = e.RecognitionResult.TopString.Length;

  //copy the strokes from the InkEdit control into the new
  // RecognizerContext
  rc.Strokes = e.RecognitionResult.Strokes.Ink.Clone().Strokes;
  isRecoPending = true;
}

private void rc_Recognition(object sender,
Microsoft.Ink.RecognizerContextRecognitionWithAlternatesEventArgs e)
{
  if (inkEdit1.InvokeRequired)
  {
    inkEdit1.Invoke(new RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition),
      new object[] { sender, e });
    return;
  }

  //set the insertion point in the InkEdit control
  inkEdit1.SelectionStart = wlSelStart;
  inkEdit1.SelectionLength = wlSelLen;
  //insert the result from the new RecognizerContext 
  //into the InkEdit control
  inkEdit1.SelectedText = e.Result.TopString;
  inkEdit1.SelectionStart = inkEdit1.SelectionStart +
  e.Result.TopString.Length;
}

// Event handler for the form's closed event
private void Form1_Closed(object sender, System.EventArgs e)
{
  inkEdit1.Dispose();
  inkEdit1 = null;
  rc.Dispose();
  rc = null;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkEdit 控制項](/previous-versions/ms552265(v=vs.100))
</dt> <dt>

[RecognizerCoNtext 類別](/previous-versions/ms552546(v=vs.100))
</dt> <dt>

[Microsoft. 單詞表類別](/previous-versions/ms827589(v=msdn.10))
</dt> </dl>

 

 
