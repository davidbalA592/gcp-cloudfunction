# gcp-cloudfunction

def hello_gcs(event, context):
    """Triggered by a change to a Cloud Storage bucket.
    Args:
         event (dict): Event payload.
         context (google.cloud.functions.Context): Metadata for the event.
    """
    final_string = "Event ID: {} \nEvent type: {} \nBucket: {}\nFile: {}\nCreated: {}"
    print(final_string.format(context.event_id,context.event_type,event['bucket'],event['name'],event['timeCreated']))
